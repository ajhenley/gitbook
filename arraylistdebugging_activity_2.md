###ArrayList Debugging Activity 2

When working with ArrayList, you will sometimes want to obtain an actual array that contains the contents of the list. As explained earlier, you can do this by calling toArray( ). Several reasons exist why you might want to convert a collection into an array such as:

To obtain faster processing times for certain operations.
To pass an array to a method that is not overloaded to accept a collection.
To integrate your newer, collection-based code with legacy code that does not understand collections.
Whatever the reason, converting an ArrayList to an array is a trivial matter, as the following program shows:

// get array 
Object ia[] = al.toArray(); 
int sum = 0; 
// sum the array 
for(int i=0; i<ia.length; i++) 
sum += ((Integer) ia[i]).intValue(); 
System.out.println("Sum is: " + sum); 
Your mission, if you choose to accept it, is to take the code you submitted for the last activity and after all the changes are done, convert the ArrayList to an Array and output the contents of the array.


