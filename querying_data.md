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
* Look at the book class you developed earlier. Hopefully it's still in Eclipse. Look at the book table. List the features of the book class that correspond to the book table. Do you think you could populate the book class with data in the book table?