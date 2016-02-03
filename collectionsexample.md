###Collections Example
### Overview of Collections
The Java Collections API are a set of classes and interfaces. They make it easy to work with collections of objects. They work like arrays with superpowers. Their size can change dynamically, and they have more advanced behavior than arrays.

Collections come in four basic flavors:
* **Lists** contain lists of things
* **Sets** contain unique things
* **Maps** contain unique ID for each thing
* **Queues** contains things arranged in the order they are to be processed

A collection — sometimes called a container — is an object that groups multiple elements into a single unit. Collections store, retrieve, manipulate, and communicate aggregate data. Typically, they represent data items that form a natural group. Collection examples include a poker hand (collection of cards), a mail folder (letters), or a telephone directory (names and phone numbers). If you have used Java or any other programming language then you probably are familiar with collections.

To use collections in your class you must import the appropriate libraries. In this example we will be working with an ArrayList.

{%ace edit=true, lang='java'%}
import java.util.Collections;
import java.util.ArrayList;
{%endace%}

When you declare your ArrayList as Double then every object in the list must contain the same data type. You can not store primitives in the collection but you can use their object data types.

{%ace edit=true, lang='java'%}
ArrayList<Double> temperatureList = new ArrayList<Double>();
{%endace%}


Adding items to your ArrayList is simple with the add method.
{%ace edit=true, lang='java'%}
temperatureList.add(40.5);
temperatureList.add(33.9);
temperatureList.add(37.8);
temperatureList.add(15.3);
temperatureList.add(25.6); 
{%endace%}


You can print the temperatureList by passing it to
{%ace edit=true, lang='java'%}
System.out.println().
{%endace%}

{%ace edit=true, lang='java'%}
System.out.println(temperatureList);
{%endace%}
It will print as follows:
```
[40.5, 33.9, 37.8, 15.3, 25.6]
```

This doesn't give you much flexibilty so you might prefer to print with an enhanced for loop. 

{%ace edit=true, lang='java'%}
for (Double temp:temperatureList)
 {
 System.out.println(temp);
 }
{%endace%}
You can sort your list in ascending order according to the natural ordering:

{%ace edit=true, lang='java'%}
Collections.sort(temperatureList);
{%endace%}

You can search for a temperature from list. If the temperature is found then the index will be a positive number equal to the index of your item. If the temperature is not found then the index will be a number equal to the index of where the compiler would expect to find it but multiplied by -1. So, a positive number (or zero) means your element was found. A negative number means it was not found.
{%ace edit=true, lang='java'%}
 int searchIndex = Collections.binarySearch(temperatureList, 39.8);
 if(searchIndex >=0){
     System.out.println("Temperature found." + searchIndex);
 }
 else{
     System.out.println("Temperature not found." + searchIndex);
 }
{%endace%}

You can also shuffle your collection:
{%ace edit=true, lang='java'%}
Collections.shuffle(temperatureList);
{%endace%}