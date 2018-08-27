<!-- 
djw: this seems almost pointless, I'm dropping this and replacing it with a discussion of 
ArrayList vs Array and an activity to convert an app using an Array to one using an ArrayList
-->

###ArrayList Debugging Activity 2
When working with ArrayList, you will sometimes want to obtain an actual array that contains the contents of the list. As explained earlier, you can do this by calling toArray( ). 

Reasons why you might want to convert a collection into an array:
* To obtain faster processing times for certain operations.
* To pass an array to a method that is not overloaded to accept a collection.
* To integrate newer, collection-based code with legacy code that does not understand collections.

Whatever the reason, converting an ArrayList to an array is a trivial matter. 
The following program shows how:

{%ace edit=true, lang='java'%}
// get array 
Object ia[] = al.toArray(); 

int sum = 0; 

// sum the array 
for(int i=0; i<ia.length; i++){ 
    sum += ((Integer) ia[i]).intValue(); 
}
System.out.println("Sum is: " + sum); 

{%endace%}

###What happens now?
Your mission, if you choose to accept it, is to take the code you submitted for the last activity and after all the changes are done, convert the ArrayList to an Array and output the contents of the array.


