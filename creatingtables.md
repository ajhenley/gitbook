###Creating Tables
In the introduction I said that you can do "Create Read Update Delete" operations to the data inside tables. How do you make the tables in the first place? By doing CRUD on the database schema. The first SQL statement to learn is ```CREATE TABLE```:

Remember how we created a book class for our application. Now we need a Book table to store our data. It should allow for the following fields: 
* SKU (stockkeeping unit - can contain numbers, dashes and possibly letters)
* Book title (text)
* Author (text)
* Description (text)
* Price (double)
* IsInStock (true/false)

You'll enter the SQL statement in SQL Developer. The SQL statement starts with CREATE TABLE followed by the table name. Then a set of parenthesis. Within the parenthesis go the fields, separated by commas. Along with each field name (which

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
