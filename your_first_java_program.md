<!--djw: done-->
<blockquote>
A journey of a thousand miles begins with a single step.
   - Laozi
</blockquote>

It is time to write your first Java program. Your program will display a message to the screen. Your program will follow in the tradition of great programmers everywhere. The "Hello, World!" program is a computer program that outputs "Hello, World!" on a display device. Being a very simple program in most programming languages, it is often used to illustrate to programmers the basic syntax for constructing a working program.

Entering instructions for a computer to follow is not easy. You must be very specific. Typos are not tolerated. Many people find this frustrating.

The computer doesn't think. That's your job. It follows the instructions you give it. Exactly.

This exercise teaches you to enter a program. It also teaches you to correctly execute that program. 

###Let's get started...
Open Eclipse. Create a Java Project called MyFirstJavaProgram. Now create a new class named HelloWorld. In this class, type the following code. It is important to enter the code exactly as written, including capitalization and indentation. I'll explain it line by line.

{%ace edit=false, lang='java'%}
public class HelloWorld
 {
    public static void main( String[] args )
    {
        System.out.println( "Hello, World!" );
        System.out.println("Today is July 19, 2015. I am alive!");
    }
 }
{%endace%}
 
```public class HelloWorld```
The first line starts with the word ```public``` followed by a single space then the word ```class``` followed by a single space and then the class name, ```HelloWorld```. The first letter of the class name is capitalized. The class name is made up of multiple words that are not separated by spaces. Each new word starts with a capital letter. Class names always start with a capital letter in Java.

```{``` The second line is just a single character: a “brace”. This character is to the right of the 'P'. Hold Shift while pressing the '[' key.


```public static void main( String[] args )```
The third line is the name of the method, main. Methods begin with lower case letters. If a method contains multiple words then begin each word with a capital letter and don't separate them with spaces. Main is the only method that you can't name on your own. For all other methods you'll make up a meaningful name. By convention, main is the starting point for all Java programs. You should have only one main method in your program. 

```[``` and ```]``` are called “brackets”, but many programmers call them “square brackets” to make sure there’s no confusion. In Java, parentheses and square brackets are not interchangeable. Brackets come in pairs and they are called “left bracket” or “open bracket” and “right bracket” or “close bracket”.

Parenthesis, braces and brackets always come in pairs. When you create your program you should line up matching parenthesis, braces and brackets. Notice in the above program how I have them lined up after each metnod of the class name.


```{``` and ```}``` are called “braces” or “curly braces”. They are used to group lines of code into a single block of code. 


```System.out.println( "Hello, World!" );```

```"``` is called a “quotation mark”, often just abbreviated “quote”. In Java, these always come in pairs. The first one in a pair is usually called an “open quote” and the second one is a “close quote” even though it’s the exact same character in both places. But the first quote serves to begin something and the second one ends that thing.

```'``` is technically an “apostrophe”, but almost all programmers call them “single quotes”. For this reason a quotation mark is often called a “double quote”. In some programming languages, single quotes and double quotes are interchangeable, but not in Java. Java does use single quotes sometimes, but they’re going to be pretty rare in this book.

```.``` is technically a “period”, but almost all programmers just say “dot”. They are used a lot in programming languages, and they are usually used as separators instead of “enders”, so we don’t call them periods.There are four dots in this program and one period.

```;``` is called a “semicolon”. It’s between the letter ‘L’ and the quote on the keyboard. Java statements often end in semicolons.


Compiling Your First Program
Now that the program has been written and hopefully contains no mistakes (we’ll see soon enough), run your program. Go to the Run menu and select Run this will compile and run your application. You will see the output from the application in the Console tab.


###What to do next
Add another line to the program to print your name.

###What You Should See After Completing the Study Drills

```
Hello, World!
Today is July 19, 2015. I am alive!
My name is Alton.
```
[Sample Code](https://gist.github.com/LearnByCode/fa63bcadce002dbe7084)