<!--djw:done-->
Prerequisite: Complete the SQL Bonus Practice. You will be using the tables created in that project for this one. You must create a database with multiple tables.

####Create a dynamic web application to search by last name
Create a search form that will allow users to enter a name in a text box and find all the matching last names. If the user enters partial text the application finds all last names that contain that text. So Smith will find users named Smith and Smithman.

To search for a partial term in SQL use the ```LIKE`` operator with the wildcard character ```%```. The percent sign will match any number of letters. Note that our installation of Oracle is case-sensitive. So 'smith' will not match 'Smith'.

So to find all users named Smith use the following SQL statement:

``sql
select firstname,lastname from customers where lastname like 'Smith%'
```
Once the user is found, display a page with the user's details.

####Close the database connection
Before you submit the project make sure you arer are closing the database connection. If you don't it will remain allocated. After running your project a number of times Eclipse will run out of memory. You'll get an error message from Oracle.

####Submit SQL Scripts in GitHub 
When submitting database projects to GitHub. include your SQL Scripts. You can create a folder in your project and they will be submitted to GitHub. That way if you need to rebuild your database you have the latest version under source control.