Youy just created a table. But it contains no data. You can insert data by entering it into the table from SQL Developer or by running some SQL statements. Run the following SQL statements to insert some book data into your table.

{%ace edit=true, lang='sql'%}
INSERT INTO BOOK (BookID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, UnitsInStock) VALUES (1, 'Book1', 'Fellowship of the Zombies', 'Charles Buckminster', 'A book about Zombies', '19.95', 150);
INSERT INTO BOOK (BookID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, UnitsInStock) VALUES (2, 'Book2', 'Vampire Mercury', 'Farrah Zahir', 'The Fastest Vampire known', '22.95', 17);
INSERT INTO BOOK (BookID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, UnitsInStock) VALUES (3, 'Book3', 'Everlasting Wizard', 'ita Keegan', 'The Magic Never Ends', '12.50', 99);
INSERT INTO BOOK (BookID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, UnitsInStock) VALUES (4, 'Book4', 'Night Ninja', 'Rebekah Axel', 'Office worker by day, ninja by night', '17.79', 0);
INSERT INTO BOOK (BookID, SKU, TITLE, AUTHOR, DESCRIPTION, PRICE, UnitsInStock) VALUES (5, 'Book5', 'Spirit of the Asteroid', 'Shafira Jamal', 'Being alone, cold and lonely builds character', '20.50', 10);
select * from Book;
{%endace%}
