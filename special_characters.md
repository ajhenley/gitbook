# Special characters
<!--
print a box, an oval, and a diamond using *'s
********
*      *
*      *
*      *
*      *
********

  ***  
 *   *
*     *
*     *
 *   *
  *** 



print a picture of my cat
  |\_/|       
 / @ @ \      
( > º < )     
 `>>x<<´     
 /  O  \       

what does the following print?
System.out.print("*");
System.out.println("***");
System.out.print("****");
System.out.println("*");

What does the following line of code print?
System.out.printf("%s\n%s\n%s\n","@","@@","@@@");
-->
Special Characters
Escape Sequences and Comments
Have you thought about what might happen if we wanted to display a quotation mark on the screen? Since everything we want to display is contained between quotation marks in the println() statement, putting a quote inside the quotes would be a problem.

Most programming languages allow for “escape sequences”, where you signal with some sort of escape character that the next character you see shouldn’t be handled in the normal way.

The following (evil) code demonstrates a number of Java’s escape sequences. Call it EscapeSequences.java.

```java
 1 public class EscapeSequences
 2 {
 3     public static void main( String[] args )
 4     {
 5         // Initial version created using FIGlet, font "Big Money", oriented southwest
 6 
 7         System.out.print( "\t    _____\n\t   /     |\n\t   JJJJJ |" );
 8         System.out.println( "  ______   __     __  ______" );
 9         System.out.println( "\t      JJ | /      \\ /  \\   /  |/      \\" );
10         System.out.println( "\t __   JJ | aaaaaa  |\"\"  \\ /\"\"/ aaaaaa  |" );
11         System.out.println( "\t/  |  JJ | /    aa | \"\"  /\"\"/  /    aa |" );
12         System.out.println( "\tJJ \\__JJ |/aaaaaaa |  \"\" \"\"/  /aaaaaaa |" );
13         System.out.println( "\tJJ    JJ/ aa    aa |   \"\"\"/   aa    aa |" );
14         System.out.println( "\t JJJJJJ/   aaaaaaa/     \"/     aaaaaaa/" );
15     }
16 }
```

When you run it, this is what you should see.

``` java
             _____
           /     |
           JJJJJ |  ______   __     __  ______
              JJ | /      \ /  \   /  |/      \
         __   JJ | aaaaaa  |""  \ /""/ aaaaaa  |
        /  |  JJ | /    aa | ""  /""/  /    aa |
        JJ \__JJ |/aaaaaaa |  "" ""/  /aaaaaaa |
        JJ    JJ/ aa    aa |   """/   aa    aa |
         JJJJJJ/   aaaaaaa/     "/     aaaaaaa/
```

Java’s escape character is a backslash (“\”), which is the same key you press to make a pipe (“|”) show up but without holding Shift. All escape sequences in Java must be inside a set of quotes.

 

```\"``` represents a quotation mark.

```\t``` is a tab; it is the same as if you pressed the Tab key while typing your code. It probably seems more complicated now because you’ve never seen it before, but when you’re reading someone else’s code a \t inside the quotes is less ambiguous than a bunch of blank spaces that might be spaces or might be a tab.

```\n``` is a newline. When printing it will cause the output to move down to the beginning of the next line before continuing printing.

```\\``` is how you display a backslash.

On line 5 you will notice that the line begins with two slashes (or “forward slashes”, if you insist). This marks the line as a “comment”, which is in the program for the human programmers’ benefit. Comments are totally ignored by the computer.

In fact, the two slashes to mark a comment don’t have to be at the beginning of the line; we could write something like this:

```System.out.println( "A" ); // prints an 'A' on the screen```

…and it would totally work. Everything from the two slashes to the end of that line is ignored by the compiler.

(That’s not a very good comment, though; any programmer who knows Java already knows what that line of code does. In general you should put comments explaining why the code is there, not what the code does. You’ll get better at writing good comments as you get better at coding in general.)
Anyway, this one was a tough one, so no Study Drills this time. The next exercise will feature something new and return to normal difficulty.


System.out.println("  |\_/|");
System.out.println(" / @ @ \");       
System.out.println("( > º < )");       
System.out.println(" `>>x<<´");      
System.out.println(" /  O  \");    
