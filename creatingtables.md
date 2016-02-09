<!--djw:done-->
###Creating Tables
Remember how we created a book class for our application? Now we need a Book table to store our data. It should allow for the following fields: 
* SKU (stockkeeping unit - can contain numbers, dashes and possibly letters)
* Book title (text)
* Author (text)
* Description (text)
* Price (double)
* IsInStock (true/false)

You'll enter the SQL statement in Oracle SQL Developer. The SQL statement starts with CREATE TABLE followed by the table name. Then a set of parenthesis. Within the parenthesis go the fields, separated by commas. Field names may not contain spaces. Follow each field name with a space and the data type. Close the statement with a semi-colon.

{%ace edit=true, lang='sql'%}
CREATE TABLE Book (
    BookID INTEGER PRIMARY KEY,
    SKU VARCHAR(50),
    Title VARCHAR(50),
    Author VARCHAR(50),
    Description VARCHAR(150),
    Price number(5,2),
    UnitsInStock NUMBER(3)
);
{%endace%}

####Inserting Data
If you ran the above statement in SQL Developer you would have a table that contains no data. You can insert data by entering it into the table or by running some SQL statements. Run the following SQL statements to insert some book data into your table.

{%ace edit=true, lang='sql'%}
INSERT INTO BOOK (BookID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, UnitsInStock) VALUES (1, 'Book1', 'Fellowship of the Zombies', 'Charles Buckminster', 'A book about Zombies', '19.95', 150);
INSERT INTO BOOK (BookID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, UnitsInStock) VALUES (2, 'Book2', 'Vampire Mercury', 'Farrah Zahir', 'The Fastest Vampire known', '22.95', 17);
INSERT INTO BOOK (BookID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, UnitsInStock) VALUES (3, 'Book3', 'Everlasting Wizard', 'ita Keegan', 'The Magic Never Ends', '12.50', 99);
INSERT INTO BOOK (BookID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, UnitsInStock) VALUES (4, 'Book4', 'Night Ninja', 'Rebekah Axel', 'Office worker by day, ninja by night', '17.79', 0);
INSERT INTO BOOK (BookID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, UnitsInStock) VALUES (5, 'Book5', 'Spirit of the Asteroid', 'Shafira Jamal', 'Being alone, cold and lonely builds character', '20.50', 10);
select * from Book;
{%endace%}

####Querying Data
Once you get data in your database you'll use SQL to query it and return a summary of your data. Run these two SQL statements to see how to get data out of your database.

You'll actually want to run each SQL statement one at a time. You can just highlight the statement you're interested in and press ```CTRL``` + ```Enter```.
Can you figure out what each statement does? We'll look at them again in greater detail in upcoming lessons.

{%ace edit=true, lang='sql'%}
SELECT * FROM Book;
SELECT Author, Title FROM Book order by Title;
Select count(*) from Book;
Update Book set Author = 'Rita Keegan' where ID = 3;
SELECT Author, Title FROM Book where ID = 3;
DROP TABLE Book;
{%endace%}

####Your assignment
* Look at the book class you developed earlier. Hopefully it's still in Eclipse. Look at the book table. What's similar?


