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





