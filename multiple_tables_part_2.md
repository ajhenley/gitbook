###Multiple Tables, Part 2
In the last example we had two tables, authors and books. Each record in the book table contained a field for an authorID. This allowed you to find the corresponding author for that book. But there's a problem. If a book has two authors then where do you store the second author?

####The solution: bridge tables
Change the tables you have for Authors and Books and add a third table to keep track of just the corresponding IDs.

|**Author**|
|---|
|AuthorID|
|FirstName|
|LastName|


|**Book**|
|---|
|BookID|
|Title|
|Description|
|Price|

|**AuthorBook**|
|---|
|AuthorID|
|BookID|



Now you can store the same AuthorID with multiple BookIDs. What's more, you can store the same BookID with multiple AuthorIDs.

####Your Assignment
Create the AuthorBook table. To do that run the following code in SQL Developer. Then query the three tables. This is all shown in the SQL below. I've included some comments to help clarify things.

{%ace edit=true, lang='sql'%}
--create a bridge table 
create table AuthorBook (
  AuthorBookID INTEGER PRIMARY KEY,
  AuthorID INTEGER,
  BookID INTEGER
);

--insert some data into the bridge table so we can keep track of the authors and books
insert into AuthorBook (AuthorBookID, AuthorID,BookID)values(1,1,1);
insert into AuthorBook (AuthorBookID, AuthorID,BookID)values(2,2,2);
insert into AuthorBook (AuthorBookID, AuthorID,BookID)values(3,3,3);
insert into AuthorBook (AuthorBookID, AuthorID,BookID)values(4,4,4);
insert into AuthorBook (AuthorBookID, AuthorID,BookID)values(5,5,5);

--we no longer need the key field in the Author table
alter table Book drop column AuthorID;
--see what we have just done
select * from Book;

--add a second author 
insert into Author (AuthorID,FirstName,LastName) values (6,'Bruce', 'Knox');
select * from Author;

--Bruce Knox is the co-author of Book3 so add a record into AuthorBook
insert into AuthorBook values (6,6,3);
--view the data
select * from AuthorBook;

--bring it all together. Notice Book3 is listed twice with two authors
select SKU,FirstName,LastName,Title,Description 
from Author 
inner join AuthorBook 
on Author.AuthorID = AuthorBook.AuthorID 
inner join Book
on Book.BookID = AuthorBook.BookID
order by Book.SKU;
{%endace%}

