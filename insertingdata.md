# Inserting Data

You have a couple tables to work with, so now I'll have you put some data into them using the INSERT command:

INSERT INTO person (id, first_name, last_name, age)
    VALUES (0, 'Dave', 'Wolfe', 25);

INSERT INTO pet (id, name, breed, age, dead)
    VALUES (0, "Fluffy", "Unicorn", 1000, 0);

INSERT INTO pet VALUES (1, "Gigantor", "Robot", 1, 1);
In this exercise I'm using two different forms of the INSERT command. The first form is the more explicit style, and most likely the one you should use. It specifies the columns that will be inserted, followed by VALUES, then the data to include. Both of these lists (column names and values) go inside parenthesis and are separated by commas.

The second version on line 7 is an abbreviated version that doesn't specify the columns and instead relies on the implicit order in the table. This form is dangerous since you don't know what column your statement is actually accessing, and some databases don't have reliable ordering for the columns. It's best to only use this form when you're really lazy.

What You Should See

INSERT INTO person (id, first_name, last_name, age)
    VALUES (0, 'Dave', 'Wolfe', 25);

INSERT INTO pet (id, name, breed, age, dead)
    VALUES (0, 'Fluffy', 'Unicorn', 1000, 0);

INSERT INTO pet VALUES (1, 'Gigantor', 'Robot', 1, 1);
On Your Own

Insert yourself and your pets (or imaginary pets like I have). Insert the proper entries in the Person_Pet table to show ownership.
Say I give you my dead unicorn. How do we execute that exchange?
What changes can we make to the tables to show that fluffy used to belong to me?
Make those changes