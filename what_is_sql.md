###What is Structured Query Language (SQL)?
SQL (pronounced as the letters SQL or sequel) is an abbreviation for Structured Query Language. It is a specialized database language that consists of statements that are very close to English. It has one purpose: to communicate with a database.

What is SQL?
* SQL stands for Structured Query Language 
* SQL allows you to access a database 
* SQL can execute queries against a database 
* SQL allows you to
    * retrieve data from a database 
    * insert new records in a database 
    * delete records from a database 
    * update records in a database 
* SQL is easy to learn



####What are the advantages of SQL?
* SQL is not a propriertary language used by a specific vendor. Almost every major DBMS supports SQL. Learning SQL will enable you to interact with every database you’ll run into.
* SQL is easy to learn. The statements consist of of descriptive English words.
* SQL is powerful. Cleverly using the language elements allows you to perform complex database operations.

**SQL is a Standard - BUT....**
SQL is an ANSI (American National Standards Institute) standard computer language for accessing and manipulating database systems. SQL statements allow you to retrieve and update data in a database. SQL works with database programs like MS Access, IBM DB2, Informix, Microsoft SQL Server, Oracle, Sybase, etc.

**... There are many different versions of the SQL language**
Most of the SQL database programs also have their own proprietary extensions in addition to the SQL standard!

To remain in compliance with the ANSI standard each must support the major keywords in a similar manner. This means that SELECT, UPDATE, DELETE, INSERT, WHERE alll work in the same way on most databases.

####Example SQL Statements
Copy the following SQL Statemets to Oracle SQL Developer. Run each statement one at a time. Each statement ends at the semicolon. To run a statement, select the statement and click  ```CTRL``` + ```Enter``` together.

{%ace edit=true, lang='sql'%}
select * from demo_customers;

select * from demo_orders;

select demo_customers.customer_id, cust_last_name, order_total 
from demo_customers 
inner join demo_orders on 
demo_customers.customer_id = demo_orders.customer_id
where demo_customers.customer_id between 2 and 5
order by order_total desc;

select demo_orders.ORDER_TIMESTAMP, cust_last_name, order_total 
from demo_customers 
inner join demo_orders on 
demo_customers.customer_id = demo_orders.customer_id
where demo_orders.ORDER_TIMESTAMP between '01-OCT-15' and '31-OCT-15'
order by order_total desc;

insert into demo_customers (cust_first_name,cust_last_name) values ('Bart','Simpson');
select * from demo_customers;
delete from demo_customers where cust_last_name = 'Simpson';
select * from demo_customers;
{%endace%}

