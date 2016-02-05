###Creating Tables
In the introduction I said that you can do "Create Read Update Delete" operations to the data inside tables. How do you make the tables in the first place? By doing CRUD on the database schema, and the first SQL statement to learn is CREATE:

CREATE TABLE person (
    id INTEGER PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    age INTEGER
);
You could put this all on one line, but I want to talk about each line so it's on multiple ones. Here's what each line does:

ex1.sql:1
The start of the "CREATE TABLE" which gives the name of the table as person. You then put the fields you want inside parenthesis after this setup.
ex1.sql:2
An id column which will be used to exactly identify each row. The format of a column is NAME TYPE, and in this case I'm saying I want an INTEGER that is also a PRIMARY KEY. Doing this tells SQLite3 to treat this column special.
ex1.sql:3-4
A first_name and a last_name column which are both of type VARCHAR. They both can hold up to 50 characters.
ex1.sql:5
An age column that is just a plain INTEGER.
ex1.sql:6
Ending of the list of columns with a closing parenthesis and then a semi-colon ';' character.
What You Should See

The easiest way to run this is in SQLDeveloper. What you should see is:
Table PERSON created.
Extra Credit

SQL is mostly a case-insensitive language. It was created in an era when case sensitivity was perceived as a major usability problem, so it has this quirk which can anoy the hell out of programmers from other languages. Rewrite this so that it's all lowercase and see if it still works. You'll need to delete person. Add other INTEGER and VARCHAR fields for other things a person might have.

