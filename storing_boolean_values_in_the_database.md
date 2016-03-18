###Common Built-in data type categories

|Category|Description|
|--|--|
|Character|Strings of characters|
|Numeric|Integer, decimal and floating-point numbers|
|Temporal|Dates and times|
|Large object (LOB)|Text, images and files|
|Rowid|Address for each row in the database|

####Storing text
```char(n)``` - stores a fixed-length string of n characters. The size (optional) of n can be from 1 to 2000.
```varchar2(size n)``` - stores a variable length string of characer data up to 4000 characters. Size is required.

####Storing numbers
```number(p,s)``` - stores negative and positive numbers. Precision(p) can range from 1 to 38. scale (s) can range from -84 to 127. The precision indicates the number of digits that can be stored. The scale indicates the number of decimal digits that can be stored to the right of the decimal point.

####Storing Dates

####Boolean data
Oracle doesn't have a data type called boolean for storing true/false or yes/no values. Programmers will often create a field that is of type char and use 'Y' for yes or 'N' for no. You'll also see people use the value of 0 for No or False and 1 for Yes or true. This is recommended because it will interact correctly with JDBC and other programming environments. Also, the char data type consumes less space in the database than Number.

Try it yourself
create table tbool (bool char check (bool in (0,1));
insert into tbool values(0);
insert into tbool values(1);`