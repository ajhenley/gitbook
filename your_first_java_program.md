# Your first java program

<blockquote>
A journey of a thousand miles begins with a single step.
   - Laozi
</blockquote>

It is time to write your first Java program. Your program will display a message to the screen. Your program will follow in the tradition of great programmers everywhere. The "Hello, World!" program is a computer program that outputs "Hello, World!" on a display device. Being a very simple program in most programming languages, it is often used to illustrate to beginning programmers the basic syntax for constructing a working program.

Typing detailed instructions for a computer to follow is not easy. You must be very specific. Many people find this frustrating.

You need to adapt to the computer. You need to learn to type instructions in a way to get the dumb computer to carry out your wishes. If you don't get the instructions right then the computer has no chance of getting them right either. That's what makes this hard for people.

This exercise not only teaches you to enter a program but also to correctly execute the program. 

###Let's get started...
Open Eclipse, create a Java Project called MyFirstJavaProgram. Now create a new class named FirstProg. In this class, type the following text. It is important to match what I have written exactly, including spacing, punctuation, and capitalization.

```java
public class MyFirstProgram
 {
     public static void main( String[] args )
     {
         System.out.println( "Hello, World!" );
     }
 }
```
 
I’m going to walk through this line-by-line, just to make sure you typed everything correctly.

The first line starts with the word ```public``` followed by a single space then the word ```class``` followed by a single space and then the word ```FirstProg```. The ‘F’ in “First” is capitalized, the ‘P’ in “Prog” is capitalized. There are only two capital letters in the first line. There are only two spaces.

The second line is just a single character: a “brace”. You get it to show up by holding down SHIFT and then pressing the ‘[‘ key which is usually to the right of the letter ‘P’.

Before I go on to the third line of the program, I should tell you what programmers usually call each funny symbol that appears in this program.

```(``` and ```)``` are called “parentheses” (that’s plural). Just one of them is called “a parenthesis”, but some people just call them parens (“puh-RENZ”). This one (“(“) is sometimes called a “left paren” and the other (“)”) is called a “right paren” because parentheses usually come in pairs and one is usually to the left of the other. The left parenthesis (“(“) is also often called an “open paren” and the right one is called a “close paren” for similar reasons.
There’s an open paren on line 3 and a close paren, too, and no other parentheses in the whole file.

```[``` and ```]``` are called “brackets”, but many programmers call them “square brackets” to make sure there’s no confusion. In Java, parentheses and square brackets are not interchangeable. Brackets come in pairs and they are called “left bracket” or “open bracket” and “right bracket” or “close bracket”.
There’s an open and close square bracket right next to each other on line 3.

```{``` and ```}``` are called “braces”, and some programmers call them “curly braces”. These also always come in pairs of left and right curly braces / open and close braces.

```"``` is called a “quotation mark”, often just abbreviated “quote”. In Java, these always come in pairs. The first one in a pair is usually called an “open quote” and the second one is a “close quote” even though it’s the exact same character in both places. But the first quote serves to begin something and the second one ends that thing.

```'``` is technically an “apostrophe”, but almost all programmers call them “single quotes”. For this reason a quotation mark is often called a “double quote”. In some programming languages, single quotes and double quotes are interchangeable, but not in Java. Java does use single quotes sometimes, but they’re going to be pretty rare in this book.

```.``` is technically a “period”, but almost all programmers just say “dot”. They are used a lot in programming languages, and they are usually used as separators instead of “enders”, so we don’t call them periods.There are four dots in this program and one period.

```;``` is called a “semicolon”. It’s between the letter ‘L’ and the quote on the keyboard. Java uses a lot of semicolons although there are only two of them in this program: one on the end of line 5 and another at the end of line 6.

```:``` is called a “colon”. You get it by holding SHIFT and typing a semicolon. Java does use colons, but they’re very rare.

Finally, ```<``` is a “less-than sign” and ```>``` is a “greater-than sign”, but sometimes they are used sort-of like braces or brackets. When they are used this way, they’re usually called “angle brackets”. Java uses angle brackets, but you won’t see them used in this book.

Okay, so back to the line-by-line. You have already typed the first two lines correctly.

You should start the third line by pressing TAB one time. Your cursor will move over several spaces (probably 4 or 8). Then type the word ```public``` again, one space, the word ```static```, one space, the word ```void```, one space, the word ```main``` followed by an open paren, ``` (```. Note: These is no space between the word “main” and the paren. After the paren there’s one space, the word ```String``` with a capital S, an open and close square bracket ```[]``` right next to each other, one space, the word ```args```, one space and finally a close parenthesis ```)```.

So line three starts with a tab, has a total of six spaces, and only the ‘S’ in “String” is capitalized. Whew.

On the fourth line, your text editor may have already started your cursor directly underneath the ‘p’ in “public”. If it did not do that, then you’ll have to start line 4 by pressing TAB yourself. Then just type another open curly brace and that’s it.

The fifth line should start with two tabs. Then type the word ```System``` with a capital ‘S’, then a ```.``` dot (period), then the word ```out```, another dot ```.```, the word ```println``` (pronounced “PrintLine” even though there’s no ‘i’ or ‘e’ at the end), an open paren ```(```, a space, a quotation mark ```"``` (open quote), the sentence ```I am determined to learn how to code.``` (the sentence ends with a period), then a close quote, ```"```, a space, a close paren, ```)``` and a semicolon, ```;```.

So line 5 has two tabs, nine spaces, two dots (and a period), an open and close quote, an open and close paren, and only two capital letters.

Line 6 is nearly identical to line 5 except that the sentence says ```Today's date is ``` instead of the determination sentence.

Line 7 starts with only one tab. If your text editor put two tabs in there for you, you should be able to get rid of the extra tab by pressing BACKSPACE one time. Then after the tab there’s a close curly brace, ```}```.

Finally, line 8 has no tabs and one more close curly brace, ```}```. You can press ENTER after line 8 or not: Java doesn’t care.

Everything always matches up. Notice that we have two open curly braces and two close curly braces in the file. Three open parens and three close parens. Two “open quotes” and two “close quotes”. One open square bracket and one close square bracket. This will always be true.

Also notice that every time we did an open curly brace, the line(s) below it had more tabs at the beginning, and the lines below close curly braces had fewer tabs.

Okay, now save this (if you haven’t already) as FirstProg.java.

Make sure the file name matches mine exactly: the ‘F’ in “First” is capitalized, the ‘P’ in “Prog” is capitalized, and everything else is lowercase. And there should be no spaces in the file name. Java will refuse to run any program with a space in the file name. Also make sure the filename ends in .java and not .txt.

Compiling Your First Program
Now that the program has been written and hopefully contains no mistakes (we’ll see soon enough), run your program. Go to the Run menu and select Run this will compile and run your application. You will see the output from the application in the Console tab.


### What You Should See
<pre>I am determined to learn how to code.
Today's date is</pre>

Are you stoked? You just wrote your first Java program and ran it! If you made it this far, then you almost certainly have what it takes to finish the course as long as you work on it every day and don’t quit.

### Study Drills
After most of the exercises, I will list some additional tasks you should try after typing up the code and getting it to compile and run. Some study drills will be  simple and some will be  challenging, but you should always give them a shot.

* Change what is inside the quotes on line 6 to include today’s date. Save the file once you have made your changes, compile the file and run it again.
* Change what is inside the quotes on line 5 to have the computer display your name.


### What You Should See After Completing the Study Drills

```
I, Alton Henley, am determined to learn how to code.
Today's date is Friday, July 19, 2015.
```