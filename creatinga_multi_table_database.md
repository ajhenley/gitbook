###Creating A Multi_Table Database

Creating one table helps but what if the person has a pet. Where do we store that? Now you will make three tables that you can store data into.

CREATE TABLE person (
    id INTEGER PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    age INTEGER
);

CREATE TABLE pet (
    id INTEGER PRIMARY KEY,
    name VARCHAR(50),
    breed VARCHAR(50),
    age INTEGER,
    dead INTEGER
);

CREATE TABLE person_pet (
    person_id INTEGER,
    pet_id INTEGER
);
In this exercise you are making tables for two types of data, and then "linking" them together with a third table. People call these "linking" tables "relations", but very pedantic people with no lives call all tables "relations" and enjoy confusing people who just want to get their jobs done. In my book, tables that have data are "tables", and tables that link tables together are called "relations".

There isn't anything new here, except when you look at person_pet you'll see that I've made two columns: person_id and pet_id. How you would link two tables together is simply insert a row into person_pet that had the values of the two row's id columns you wanted to connect. For example, if person contained a row with id=20 and pet had a row with id=98, then to say that person owned that pet, you would insert person_id=20, pet_id=98 into the person_pet relation (table).

We'll get into actually inserting data like this in the next few exercises.

What You Should See

You run this SQL script in the same way as before. As usual there's no signiciant output, other than the notification that the tables were created.

What You Should Do

In these tables I made a 3rd relation table to link them. How would you get rid of this relation table person_pet and put that information right into person? What's the implication of this change?
If you can put one row into person_pet, can you put more than one? How would you record a crazy cat lady with 50 cats?
Create another table for the cars people might own, and create its corresponding relation table.
Search for "oracle datatypes" in your favorite search engine. Take notes on what types you can use and other things that seem important. We'll cover more later.