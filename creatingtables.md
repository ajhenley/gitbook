<!--djw:done-->
In previous applications you would save data to your hard drive. Then you could open the file and read it back in. A database allows you to do the same thing - save data. It also includes software to ensure the integrity of your data. Your application will communicate with the database by sending SQL queries through the data access API. In this course, you'll use the Java ODBC  connection library for this. When the database receives the SQL it will process the query and return the results.  For now you'll use SQL Developer to submit your queries and receive the results.

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

####The Primary key
The primary key is an indicator that tells the database which field will uniquely identify each record. This makes the database operate more efficiently. Data in the primary key is most often numeric and must be unique to each record (row).


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
* Look at the book class you developed earlier. Hopefully it's still in Eclipse. Look at the book table. List the features of the book class that are correspond to the book table.


