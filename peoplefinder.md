<!--djw:done-->
###People Finder: A Dynammic Web Application with a Search Form
Prerequisite: Complete the SQL Bonus Practice. You will be using the tables created in that project for this one. You must create a database with multiple tables in order to get credit for this application.

Create a dynamic web application. This project must be it's own dynamic web application. It may not be a part of another application.

Create a search form that will allow users to enter a term in a text box and find all the matching last names. If the user enters partial text then the application shall find all companies or last names that contain that text. So Smith will find users named Smith and Smithman.

To search for a partial term in SQL use the ```LIKE`` operator with the wildcard character ```%```. The percent sign will match any number of letters. Note that our installation of Oracle is case-sensitive. So 'smith' will not match 'Smith'.

So to find all users named Smith use the following SQL statement:

``sql
select firstname,lastname from customers where lastname like 'Smith%'
```

Once the user is found, display a page with the user's details.

Before you submit the project make sure your are closing the database connection. If you don't it will remain allocated. After running your project a number of times Eclipse will run out of memory and you'll get an error message from Oracle.

When submitting database projects to GitHub. include your SQL Scripts. You can create a folder in your project and they will be submitted to GitHub. That way if you need to rebuild your database you have the latest version under source control.