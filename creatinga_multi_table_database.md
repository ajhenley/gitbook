###Creating A Multi_Table Database

In the previous exercise we combined the authors and books in one table. This would work for a small database. But it's not appropriate for enterprise applications. It's more common to have a separate table for authors and a separate table for books. This makes your database more efficient, robust and easier to query. Let's see how we could make that work.

####Create the Books table
We can use every field from our previous table except the Author field. Create that table first.
* SKU (stockkeeping unit - can contain numbers, dashes and possibly letters)
* Book title (text)
* Description (text)
* Price (double)
* IsInStock (true/false)

####Create the Authors table
We would like to keep the author's first and last names separate so we can query by last name.
* FirstName (text)
* LastName (text)
* Address (text)
* City (text)
* State (text)
* ZIP (text)
 


