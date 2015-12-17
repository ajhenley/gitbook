# Comments

<h3>Comments and Slashes</h3>

Newsflash: Your memory doesn't work. If you don't believe me then find a program you've written over 6 months or a year ago. Now go through it line by line. Explain to another person the reasons for each line of code in the program. Try doing that with somebody's else's program. Now try doing that to a program that contains lots of comments.

**Code tells you how. Comments tell you why.**

**Comments are very important in your programs.** They tell you what something does in English. And why.

**Comments can also be used for debugging**.They can be used to disable parts of your program temporarily. Just comment out a section of code and it won't run.

####Here's how you use comments in Java:
```java
public class CommentsAndSlashes
{
    public static void main( String[] args )
    {
        // A comment, this is so you can read your program later.
        // Anything after the // is ignored by Java.
        System.out.println( "This line will print." ); // this comment is ignored by the compiler.
        // You can also use a comment to "disable" or comment out a piece of code:
        // System.out.println("This line won't print.");
        System.out.println( "This line will print." );
    }
}
```


Programs should be written for people to read. Your code will spend most of its life in maintenance mode. That means a lot of your coworkers - some who may not even be born yet - will have the pleasure of maintaining your program. It's up to you to make sure it's a pleasure.

###What You Should Do on Your Own
Assignments turned in <em>without</em> these things will not receive any points. For this exercise, do these things.

1. Were you right about what the two slashes ('//') signify? Answer in a comment at the top of the file (above the ```public class```  line).
2. Add another comment at the **very** top of the file (above your answer to the previous question) with your name and today's date.
3. Insert a multiline comment. Do you know how to do that? Why not?