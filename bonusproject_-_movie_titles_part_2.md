<!--djw:done-->
###Bonus Project - Movie Titles Part 2

###Get a Movie title from the database
Modify your project for Movie Title Generator. Now, store the movie titles in the database. You can copy the word lists to Excel and import them into tables into SQL Developer. (Right click your connection and select Import). You'll need two tables.

The following sql code shows how to return a random record from a table. Change the name of the table from demo_orders to the table that contains your movie titles.

{%ace edit=true, lang='java'%}
SELECT * FROM (SELECT * FROM demo_orders ORDER BY DBMS_RANDOM.RANDOM) WHERE rownum =1;
{%endace%}

Next, create a table to store your movie titles. Include a description. After the user selects the movie title prompt for a description. Then insert the title and description into the database.