###Line item invoice assignment
Create an application that allows users to create an invoice. Your application will prompt the user for the quantity and price. Your application will then apply the tax of 6% and print a subtotal of the items and the tax and a grand total of those two amounts. The user should be able to enter as many items as desired.

```
Enter the Quantity: 2
Enter the Price: 500.00
Do you want to enter another item (y/n)? y
Enter the Quantity: 3
Enter the Price: 300.00
Do you want to enter another item (y/n) n

You invoice is:

Number of items: 5
Subtotal: 1900.00
Tax (6%): 114.00
Grand Total: 2014.00
```

####Notes
* Your completed solution should use multiple classes
* Most of your code should **not** be in the main() method. It should be in classes.
* Users should be able to input data until they run out
* The application will print out an invoice of all the data including a subtotal, tax and grand total.

####Bonus: 
Add an extra field to the inputs (untaxable). This value will be inputted as either true or false. This will affect whether tax will be charged on that item or not. 

####Bonus 2:
Format the dollar figures appropriately using the NumberFormat class discussed previously.


 
