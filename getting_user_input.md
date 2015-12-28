<!--
introduce the scanner object for getting user input and show how variables store that input.

what is your name, quest, favorite color? 
-->
###Getting and storing user input
scanner object allows people to input data. It's a simple text scanner which can parse primitive types and strings. 

A Scanner breaks its input into tokens using a delimiter pattern. The default delimiter is a space. The resulting tokens may then be converted into values of different types using the various next methods.

Here's how you use the scanner to read an integer:

```java
     Scanner sc = new Scanner(System.in);
     int i = sc.nextInt();
```
Because the scanner is only reading the next token the end-of-line(EOL) character is not read. To clear out any remaining data call ```sc.nextLine();```

variables allow the program to retain data


print allows the program to display the data

