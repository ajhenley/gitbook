<!-- todo: add a program at the bottom for the reader to add comments to, or use one of their assignments -->
####Comments

Newsflash: Your memory doesn't work. If you don't believe me then find a program you've written over 6 months or a year ago. Now go through it line by line. Explain to another person the reasons for each line of code in the program. 

Try doing that with somebody's else's program. 

Now try doing that to a program that contains lots of comments.

What kind of programmer do you want to be?

**Code tells you how. Comments tell you why.**

**Comments are very important in your programs.** They tell you what something does in English. And why.

**Comments can also be used for debugging**.
Some programmers will comment out a line of code temporarily while they debug the remaining lines. This enables you to focus on what matters and selectively ignore parts of your program.

####Here's how you use comments in Java:
```java
public class CommentsEverywhere
{
    public static void main( String[] args )
    {
        // This line will be ignored by the compiler
        // but people will (hopefully) read it. 
        // Anything after the // is ignored by Java.
        System.out.println( "This line prints just fine." ); // I can include a comment after the working code..
        // This next line of code has been disabled by a comment:
        // System.out.println("This line won't print.");
        System.out.println( "This line also prints just fine." );
    }
}
```


Programs should be written for people to read. Your code will spend most of its life in maintenance mode. That means a lot of your coworkers - some who may not even be born yet - will have the pleasure of maintaining your program. It's up to you to make sure it's a pleasure.

<blockquote>
The practitioner of literate programming can be regarded as an essayist, whose main concern is with exposition and excellence of style. Such an author, with thesaurus in hand, chooses the names of variables carefully and explains what each variable means. He or she strives for a program that is comprehensible because its concepts have been introduced in an order that is best for human understanding, using a mixture of formal and informal methods that reinforce each other.
 - Donald Knuth, Literate Programming. 1992.
</blockquote>


###Your assignment
* Go through the code below and add comments where you see two slashes. Make sure the code still runs.
 *Add a multi-line comment at the top of the program that contains your name, the date and the name of the program.


