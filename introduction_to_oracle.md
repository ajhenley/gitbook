###Working with Oracle: the big picture
Let's talk about how Oracle and Java work together to get data from where it's stored and back to the user.  We begin with general concepts you may hear from other books or upcoming assignments.We'll then look into some specific topics in greater detail.

What is a client/server system?

How does the client access the server?

####What is JDBC?
Java Database Connectivity (JDBC) is an application programming interface (API). It determines how a Java program may access a database such as Oracle. Think of JDBC as the communication channel between your Java application and Oracle. The program will request some data, Oracle will fufill that request and the program will receive the result. 

####What is a relational database and why do we need one?
A relational database organizes data in tables. Tables contain records (rows) and fields (columns). Corresponding records are linked through key fields called Primary Keys and Foreign Keys. For example, Managers, Departments and Salary information are stored in different tables. Relationships between the tables permit one to find corresponding records. This allows one to can determine the average salary of the managers of every department.

A database is an organized collection of data. It allows for efficient storage and retrieval of data. Key features of a Database Management System (DBMS):
* Minimizes redundancy of data
* Permits sharing among users
* Maintains consistency of data even against simultaneous updates
* Enforces data validity and constraints
* Restricts access as needed
* Permits backup and recovery from data loss




What is SQL?

What is a database schema?

What is a table?
* joining tables

What are indexes and keys?

What is a sequence?

How is data related?
one-to-one
one-to-many
many-to-many


You can do CRUD (Create, Read, Update, Delete) operations to the data inside tables.