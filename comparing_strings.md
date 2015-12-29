<!--rewrite this-->
# Comparing strings

Comparing Strings
In this exercise we will see something that causes trouble for beginners trying to learn Java: the regular relational operators do not work with Strings, only numbers.
```
boolean a, b;
a = ("cat" < "dog");
b = ("horse" == "horse" );
The second line doesn’t even compile! You can’t use < to see if a word comes before another word in Java. And in the third line, b does get set to the value true here, but not if you read the value into a variable like so:

String animal;
animal = keyboard.next(); // the user types in "horse"
b = ( animal == "horse" );
b will always get set to the value false, no matter if the human types "horse" or not!

I don’t want to try to explain why this is. The creators of Java do have a good reason for this apparently weird behavior, but it’s not friendly for beginners and explaining it would probably only confuse you more at this point in your learning.

Do you remember when I warned you that Java is not a language for beginners?

So there is a way to compare Strings for equality, so let’s look at it.

 1 import java.util.Scanner;
 2 
 3 public class WeaselOrNot
 4 {
 5     public static void main( String[] args )
 6     {
 7         Scanner keyboard = new Scanner(System.in);
 8 
 9         String word;
10         boolean yep, nope;
11 
12         System.out.println( "Type the word \"weasel\", please." );
13         word = keyboard.next();
14 
15         yep  =   word.equals("weasel");
16         nope = ! word.equals("weasel");
17 
18         System.out.println( "You typed what was requested: " + yep );
19         System.out.println( "You ignored polite instructions: " + nope );
20     }
21 }```

####What You Should See
```
Type the word "weasel", please.
no
You typed what was requested: false
You ignored polite instructions: true
```

So Strings have a built-in method named .equals() (“dot equals”) that compares itself to another String, simplifying to the value true if they are equal and to the value false if they are not. And you must use the not operator (!) together with the .equals() method to find out if two Strings are different.

###Study Drills
Try changing around the comparison on line 15 so that "weasel" is in front of the dot and the variable word is inside the parentheses. Make sure that "weasel" is still surrounded by quotes and that word is not. Does it work?