<!-- djw:done -->
###Getting and storing user input
scanner object allows people to input data. It's a simple text scanner which can parse primitive types and strings. 

A Scanner scans the input by tokens using a delimiter pattern. The default delimiter is a space. So the scanner reads the input token by token. The resulting tokens may then be converted into values of different types using various methods.

####Methods of the Scanner class

|Method|Returns|
|-|-|
|int nextInt()|Returns the next token as an int. |
|long nextLong()|Returns the next token as a long.|
|float nextFloat()|Returns the next token as a float.| 
|double nextDouble()|Returns the next token as a long.| 
|String next()|Finds and returns the next complete token from this scanner and returns it as a string; a token is usually ended by whitespace such as a blank or line break. If no token exists, NoSuchElementException is thrown.|
|String nextLine()|Returns the rest of the current line, excluding any line separator at the end.|
|void close()|Closes the scanner object.

####Here's how you use the scanner to read an integer:

```java
     Scanner sc = new Scanner(System.in);
     int i = sc.nextInt();
```
Because the scanner is only reading the next token, the end-of-line(EOL) character is not read. To clear out any remaining data call ```sc.nextLine();``` which will read to the end of the line.



####Your assignment
Create a program that prompts the user for their name, their quest and their favorite color. Store the value of each response in a variable. Display the answers after the questions have been asked.

