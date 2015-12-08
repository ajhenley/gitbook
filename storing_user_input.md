# Storing user input

Storing the Human’s Responses
In the last exercise, you learned how to pause the program and allow the human to type in something. But what happened to what was typed? When you typed in the answer “Paris” for the first question, where did that answer go? Well, it was thrown away right after it was typed because we didn’t put any instructions to tell the Scanner object where to store it. So that is the topic of today’s lesson.
<pre>
 1 import java.util.Scanner;
 2 
 3 public class RudeQuestions
 4 {
 5     public static void main( String[] args )
 6     {
 7         String name;
 8         int age;
 9         double weight, income;
10 
11         Scanner keyboard = new Scanner(System.in);
12 
13         System.out.print( "Hello. What is your name? " );
14         name = keyboard.next();
15 
16         System.out.print( "Hi, " + name + "! How old are you? " );
17         age = keyboard.nextInt();
18 
19         System.out.println( "So you're " + age + ", eh? That's not old at all." );
20         System.out.print( "How much do you weigh, " + name + "? " );
21         weight = keyboard.nextDouble();
22 
23         System.out.print( weight + "! Better keep that quiet. Finally, what's your income, " + name + "? " );
24         income = keyboard.nextDouble();
25 
26         System.out.println( "Hopefully that is " + income + " per hour and not per year!" );
27         System.out.println( "Well, thanks for answering my rude questions, " + name + "." );
28     
29         keyboard.close();//close the scanner to release the resources
30    }
31  }
</pre>
Just like the last exercise, when you first run this your program will only display the first question and then pause, waiting for a response:

Hello. What is your name?
Notice that because that first printing statement on line 13 is print() rather than println(), the cursor is left blinking at the end of the line the question is on. If you had used println(), the cursor would blink on the beginning of the next line instead.

What You Should See
<pre>Hello. What is your name? Brick
Hi, Brick! How old are you? 25
So you're 25, eh? That's not old at all.
How much do you weigh, Brick? 192
192.0! Better keep that quiet. Finally, what's your income, Brick? 8.75
Hopefully that is 8.75 per hour and not per year!
Well, thanks for answering my rude questions, Brick.
</pre>
At the top of the program we declared four variables: one String variable named name, one integer variable named age, and two double variables named weight and income.

On line 14 we see the keyboard.next() that we know from the previous exercise will pause the program and let the human type in something it will package up in a String. So now where does the String they type go? In this case, we are storing that value into the String variable named “name”. The String value gets stored into a String variable. Nice.

So, assuming you type Brick for your name, the String value "Brick" gets stored into the variable name on line 14. This means that on line 16, we can display that value on the screen! That’s pretty cool, if you ask me.

On line 17 we ask the Scanner object to let the human type in something which it will try to format as an integer, and then that value will be stored into the integer variable named age. We display that value on the screen on line 19.

Line 21 reads in a double value and stores it into weight, and line 24 reads in another double value and stores it into income.

This is a really powerful thing. With some variables and with the help of the Scanner object, we can now let the human type in information, and we can remember it in a variable to use later in the program!

Before I wrap up, notice for example that the variable income is declared all the way up on line 9 (we choose its name and type), but it is undefined (it doesn’t have a value) until line 24. On line 24 income is finally initialized (given its first value of the program). If you had attempted to print the value of income on the screen prior to line 24, the program would not have compiled.

Anyway, play with typing in different answers to the questions and see if you can get the program to blow up after each question.