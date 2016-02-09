###Import Customers Table

####Instructions for obtaining the customers.xlsx file

1. Download the customers.xlsx file. It's an Excel file containing 30,000 rows of data. 
2. Import the customers file into Oracle
2. Write a query to find the number of people living in each state
3. Write a query to find the the number of unique companies in the table
4. Create a new table for companies and move that data to the new table. Only move the unique companies. Then add a column to your customers table and update the CompanyID.
5. To set the value of your unique ID you can either create a sequence and a trigger or you can simply update that column to the row number as follows: ```Update Company set CompanyId = rownum``` 
6. Create a new table for cities and states and move that data to the new table in the same way you did above. Move unique cities/states to the new table. 
7. Delete those columns from this table and add keys to link to the new tables
8. Create a query that recreates the list in Excel using joined tables.
9. Finally, export the data as SQL import statements


Some help for you......
you want to move all the unique company names to another table 
and then delete them from the customer table.
select distinct company from customers 
alter table customers add CompanyID int
select rownum,company from customers
select CompanyId from customers
create table Companies (company varchar(50));
insert into Companies select distinct company from customers;
alter table Companies add CompanyId int
update Companies set companyid=rownum
select * from Companies
alter table customers add CompanyId int
update customers c set c.companyID = (select t.companyID from
Companies t where t.company=c.company)
select c.companyID,c.company,t.companyID,t.Company from
customers c inner join Companies t on c.CompanyID=t.CompanyID
--alter table customers drop company column
select * from customers
select * from customers c inner join companies t on c.companyId=t.companyId