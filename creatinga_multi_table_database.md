###Creating A Multi_Table Database

In the previous exercise we combined the authors and books in one table. This would work for a small database. But it's not appropriate for enterprise applications. It's more common to have a separate table for authors and a separate table for books. This makes your database more efficient, robust and easier to query. Let's see how we could make that work.

####Create the Books table
We can use every field from our previous table except the Author field. Create that table first.
* SKU (stockkeeping unit - can contain numbers, dashes and possibly letters)
* Book title (text)
* Description (text)
* Price (double)
* IsInStock (true/false)

{%ace edit=true, lang='sql'%} 
CREATE TABLE Book (
    BookID INTEGER PRIMARY KEY,
    SKU VARCHAR(50),
    Title VARCHAR(50),
    Author VARCHAR(50),
    AuthorID INTEGER,
    Description VARCHAR(150),
    Price number(5,2),
    UnitsInStock NUMBER(3)
);

INSERT INTO BOOK (BookID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, UnitsInStock) VALUES (1, 'Book1', 'Fellowship of the Zombies', 'Charles Buckminster', 'A book about Zombies', '19.95', 150);
INSERT INTO BOOK (BookID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, UnitsInStock) VALUES (2, 'Book2', 'Vampire Mercury', 'Farrah Zahir', 'The Fastest Vampire known', '22.95', 17);
INSERT INTO BOOK (BookID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, UnitsInStock) VALUES (3, 'Book3', 'Everlasting Wizard', 'ita Keegan', 'The Magic Never Ends', '12.50', 99);
INSERT INTO BOOK (BookID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, UnitsInStock) VALUES (4, 'Book4', 'Night Ninja', 'Rebekah Axel', 'Office worker by day, ninja by night', '17.79', 0);
INSERT INTO BOOK (BookID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, UnitsInStock) VALUES (5, 'Book5', 'Spirit of the Asteroid', 'Shafira Jamal', 'Being alone, cold and lonely builds character', '20.50', 10);

select * from Book;
{%endace%}

####Create the Authors table
We would like to keep the author's first and last names separate so we can query by last name.
* FirstName (text)
* LastName (text)
* Address (text)
* City (text)
* State (text)
* ZIP (text)

{%ace edit=true, lang='sql'%}
CREATE TABLE Author (
  AuthorID INTEGER PRIMARY KEY,
  FirstName VARCHAR(50) default NULL,
  LastName VARCHAR(50) default NULL,
  Street VARCHAR(100) default NULL,
  City VARCHAR(50) default NULL,
  "State" VARCHAR(2) default NULL,
  Zip VARCHAR(10) default NULL
);

insert into Author (AuthorID,FirstName,LastName) values (1,'Charles', 'Buckminster');
insert into Author (AuthorID,FirstName,LastName) values (2,'Farrah', 'Zahir');
insert into Author (AuthorID,FirstName,LastName) values (3,'Rita', 'Keegan');
insert into Author (AuthorID,FirstName,LastName) values (4,'Rebekah', 'Axel');
insert into Author (AuthorID,FirstName,LastName) values (5,'Shafira', 'Jamal');
{%endace%}


####Bringing the Authors and Books together again
The following SQL statement will allow you to query the Author and Book table and bring the data back together again.

{%ace edit=true, lang='sql'%}
select SKU,FirstName,LastName,Title,Description from Author inner join Book on Author.AuthorID = Book.AuthorID order by Author.LastName;
{%endace%}

####Why did we make two tables?
It's possible some authors would write more than one book. When there was one book table then each book had the author listed with it. Stephen King has written 54 novels. The single-table database would store his name 54 times. Databases don't like to store redundant data. One of the key rules of databases is that each piece of data is in one place only. His name would belong in the Author table only. It's easier to store, update and query that way.

The database keeps track of the corresponding records with Primary Keys and Foreign Keys. The AuthorID is the primary key when it's in the Author table. It's the foreign key when it's in the Book table.




