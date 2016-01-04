# A first look at arrays

An array is a container object that holds a fixed number of values of a single type. An array can hold any type of object: integers, numbers, Strings, and even those we haven't learned about yet.

The size (called length) of an array is established when the array is created. After creation, its length is fixed.

* The first item of an array has an index value of 0
* The length of an array is equal to the number of elements in the array
* The last item of an array has an index value of one less than the number of elements
* An array's length is fixed. You can change the value of the items but you can't add any new items
* All items in the array have the same data type that was declared when the array was created

####How to declare an array
```java
double[] temperatures;
String[] args;
```
Note: it is legal to say ```String args[]``` but ```String[] args`` is more readable.

After you declare the array you need to construct the array and assign it to the variable you just declared.
```java
temperatures = new double[15];
```
Now you have an array of temperatures that can hold 15 values;

 
####Things we can do with arrays
```java 
import java.util.Array

public ArrayDemo
{
    public static void main(String args[])
    {
        //Declare array
        //Initialize elements of an array
        //Print the elements of an array
        //print one element
        //Print every other element
        //Print the number of elements
        //Change an element
        //Change all the elements
        //Copy an array
        //Search for an element
        //Sort an array
    }
}
```