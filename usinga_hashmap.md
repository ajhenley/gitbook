###Using a HashMap
A Map cares about unique identifiers. You map a unique key to a specific value. Both the key and the value are objects. A HashMap  is an unsorted, unordered Map. When you need a Map and the order of the values is the least of your worldly concerns, the HashMap is here to serve you.

####What can you do with a Hashmap?
* Search for a value based on the key
* Retrieve a collection of just keys or just values
* Add a value to be located by a key
* Delete a value by its corresponding key
* A HashMap can contain one ```null``` key and any number of ```null``` values

####How do you declare a HashMap?
The following will create a HashMap called MyMap with the keys as String and the values as String
```java
import java.util.HashMap;
HashMap<String, String> myMap = new HashMap<String, String>();
```

{%ace edit=true, lang='java'%}
import java.util.HashMap;

public class HashmapApp
{
	public static void main( String[] args )
	{
		HashMap<String,String> map = new HashMap<String,String>();

		map.put( "cat", "Meow" );
		map.put( "pig", "Oink" );
		map.put( "dog", "Woof" );
		map.put( "bat", "Squeak" );
		
		System.out.println( "map = " + map );
		System.out.println();
		System.out.println("A cat says... " + map.get("cat"));
		System.out.println("A pig says... " + map.get("pig"));
		System.out.println("A dog says... " + map.get("dog"));
		System.out.println("A bat says... " + map.get("bat"));

	}
}
{%endace%}


