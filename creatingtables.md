###Creating Tables
In the introduction I said that you can do "Create Read Update Delete" operations to the data inside tables. How do you make the tables in the first place? By doing CRUD on the database schema. The first SQL statement to learn is ```CREATE TABLE```:

{%ace edit=true, lang='sql'%}
CREATE TABLE person (
    id INTEGER PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    age INTEGER
);
{%endace%}

You could put this all on one line, but I want to talk about each line so it's on multiple ones. Here's what each line does:

Line 1: The start of the "CREATE TABLE" which gives the name of the table as person. You then put the fields you want inside parenthesis after this setup.

Line 2: An id column is to uniquely identify each row. It's possible to have two people with the same first name, last name and age. We distinguish the two matching records with a unique identifier. If using a unique identifier like employeeID then you could use that. Most DBAs (database administrators) would still create a primary key. It aids in efficiency.
The format of a column is NAME then TYPE. In this case I'm saying I want an INTEGER that is also a PRIMARY KEY. A primary key must be unique in the database. The database software will help enforce that. If you have person number 7 and you delete them (sorry, Mr. Bond) then there will never be another person number 7 in that database again.

Lines 3-4: A first_name and a last_name column which are both of type VARCHAR. They both can hold up to 50 characters.

Line 5:
An age column that is just a plain INTEGER.

Line 6:
Follow your last column with a closing parenthesis and then a semi-colon ';' character.

The easiest way to run this is in SQLDeveloper. What you should see is:
```
Table PERSON created.
```

SQL is a case-insensitive language. It was created in an era when case sensitivity was perceived as a major usability problem. 

####Your assignment
Rewrite this so that it's all lowercase and see if it still works. You'll need to delete the person table first. Do that with the following statement: ```drop table person```.

Once you recreate the person table add other INTEGER and VARCHAR fields for other things a person might have.

