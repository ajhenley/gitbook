Out of the CRUD matrix we have only covered "Create". You can create tables and you can create rows in those tables. I'll now show you how to "Read" or in the case of SQL, SELECT:

SELECT * FROM person;

SELECT name, age FROM pet;

SELECT name, age FROM pet WHERE dead = 0;

SELECT * FROM person WHERE first_name != 'Dave';
Here's what each of these lines does:

line:1
This says "select all columns from person and return all rows." The format for SELECT is SELECT what FROM tables(s) WHERE (tests) and the WHERE clause is optional. The '*' (asterisk) character is what says you want all columns.
line:3
In this one I'm only asking for two columns name and age from the pet table. It will return all rows.
line:5
Now I'm looking for the same columns from the pet table but I'm asking for only the rows where dead = 0. This gives me all the pets that are alive.
line:7
Finally I'm selecting all columns from person just like in the first line, but now I'm saying only if they do not equal "Zed". That WHERE clause is what determines which rows to return or not.
 

What You Should Do

Write a query that finds all pets older than 10 years. 
Write a query to find all people younger than you. 
Do one that's older. 
Write a query that uses more than one test in the WHERE clause using the AND to write it. For example, WHERE first_name = "Dave" AND age > 30. 
Do another query that searches for rows using 3 columns and uses both AND and OR operators.