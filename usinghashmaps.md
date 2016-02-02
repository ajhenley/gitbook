###Using Hashmaps

Link to Slides http://web.stanford.edu/class/archive/cs/cs106a/cs106a.1124/lectures/18/Slides.pdf (Links to an external site.)
Create a map and store integers and their word values.
HashMap<Integer, String> myMap = new HashMap<Integer, String>();
Prompt user to enter a number and print out the word value. 
Example:

Prompt: Enter a number: 10
Response: You entered ten.
Would you like to try again? Y/N
If number is not found (use myMap.containsKey(10) then prompt user to tell the map to add that to the map.

Add the key and value to the map with the following line of code:

myMap.put(10,"ten");

Retrieve the value with

String value = myMap.get(10)

