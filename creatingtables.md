###Creating Tables
In the introduction I said that you can do "Create Read Update Delete" operations to the data inside tables. How do you make the tables in the first place? By doing CRUD on the database schema. The first SQL statement to learn is ```CREATE TABLE```:

Remember how we created a book class for our application. Now we need a Book table to store our data. It should allow for the following fields: 
* SKU (stockkeeping unit - can contain numbers, dashes and possibly letters)
* Book title (text)
* Author (text)
* Description (text)
* Price (double)
* IsInStock (true/false)

You'll enter the SQL statement in Oracle SQL Developer. The SQL statement starts with CREATE TABLE followed by the table name. Then a set of parenthesis. Within the parenthesis go the fields, separated by commas. Field names may not contain spaces. Follow each field name with a space and the data type. Close the statement with a semi-colon.

{%ace edit=true, lang='sql'%}
CREATE TABLE book (
    id INTEGER PRIMARY KEY,
    sku VARCHAR(50),
    title VARCHAR(50),
    author VARCHAR(50),
    description VARCHAR(150),
    price number(5,2),
    isInStock char(1)
);
{%endace%}

If you ran the above statement in SQL Developer you would have a table that contains no data. You can insert data by entering it into the table or by running some SQL statements. Run the following SQL statements to insert some book data into your table.

{%ace edit=true, lang='sql'%}
INSERT INTO "SYSTEM"."BOOK" (ID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, ISINSTOCK) VALUES ('1', 'Book1', 'Fellowship of the Zombies', 'Charles Buckminster', 'A book about Zombies', '19.95', 'Y')
INSERT INTO "SYSTEM"."BOOK" (ID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, ISINSTOCK) VALUES ('2', 'Book2', 'Vampire Mercury', 'Farrah Zahir', 'The Fastest Vampire known', '22.95', 'Y')
INSERT INTO "SYSTEM"."BOOK" (ID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, ISINSTOCK) VALUES ('3', 'Book3', 'Everlasting Wizard', 'ita Keegan', 'The Magic Never Ends', '12.50', 'Y')
INSERT INTO "SYSTEM"."BOOK" (ID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, ISINSTOCK) VALUES ('4', 'Book4', 'Night Ninja', 'Rebekah Axel', 'Office worker by day, ninja by night', '17.79', 'Y')
INSERT INTO "SYSTEM"."BOOK" (ID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, ISINSTOCK) VALUES ('5', 'Book5', 'Spirit of the Asteroid', 'Shafira Jamal', 'Being alone, cold and lonely builds character', '20.50', 'Y')
{%endace%}
