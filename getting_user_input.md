# Getting user input

####Getting Input from a Human
Now that we have practiced creating variables for a bit, we are going to look at the other part of interactive programs: letting the human who is running our program have a chance to type something.

Go ahead and type this up, but notice that the first line in the program is <em>not</em> the public class line. This time we start with an &ldquo;import&rdquo; statement.

Not every program needs to get interactive input from a human using the keyboard, so this is not part of the core of the Java language. Just like a Formula 1 race car does not include an air conditioner, programming languages usually have a small core and then lots of optional libraries that can be included if desired.

```java
 1 import java.util.Scanner;
 2 
 3 public class ForgetfulMachine
 4 {
 5     public static void main( String[] args )
 6     {
 7         Scanner keyboard = new Scanner(System.in);
 8 
 9         System.out.println( "What city is the capital of France?" );
10         keyboard.next();
11 
12         System.out.println( "What is 6 multiplied by 7?" );
13         keyboard.nextInt();
14 
15         System.out.println( "What is your favorite number between 0.0 and 1.0?" );
16         keyboard.nextDouble();
17 
18         System.out.println( "Is there anything else you would like to tell me?" );
19         keyboard.next();
20     }
21 }
```

When you first run this program, it will only print the first line:
```What city is the capital of France?```

&hellip;and then it will blink the cursor at you, waiting for you to type in a word. When I ran the program, I typed the word &ldquo;Paris&rdquo;, but the program will work the same even if you type a different word.

Then after you type a word and press Enter, the program will continue, printing:
```What is 6 multiplied by 7?```

&hellip;and so on. Assuming you type in reasonable answers to each question, it will end up looking like this:

####What You Should See
```
What city is the capital of France?
Paris
What is 6 multiplied by 7?
42
What is your favorite number between 0.0 and 1.0?
2.3
Is there anything else you would like to tell me?
No, there is not.
```

So let us talk about the code. On line 1 we have an import statement. The library we import is the scanner library java.util.Scanner (&ldquo;java dot util dot Scanner&rdquo;). This library contains functionality that allows us to read in information from the keyboard or other places like files or the Internet.

Lines 2 through 7 are hopefully boring. On line 8 we see something else new: we create a &ldquo;Scanner object&rdquo; named &ldquo;keyboard&rdquo;. (It doesn&rsquo;t have to be named &ldquo;keyboard&rdquo;; you could use a different word there as long as you use it everywhere in your code.) This Scanner object named keyboard contains abilities we&rsquo;ll call functions or &ldquo;methods&rdquo;. You must create and name a Scanner object before you can use one.

On line 10 we ask the Scanner object named keyboard to do something for us. We say &ldquo;Keyboard, run your next() function.&rdquo; The Scanner object will pause the program and wait for the human to type something. Once the human types something and presses Enter, the Scanner object will package it into a String and allow your code to continue.

On line 13 we ask the Scanner object to execute its nextInt() function. This pauses the program, waits for the human to type something and press Enter, then packages it into an integer value (if possible) and continues.

What if the human doesn&rsquo;t type an integer here? Try running the program again and type 41.9 as the answer to the second question.

The program blows up and doesn&rsquo;t run any other statements because 41.9 can <em>not</em> be packaged into an integer value: 41.9 is a double. Eventually we will look at ways to handle error-checking for issues like this, but in the meantime, if the human types in something incorrectly which blows up our program, we will blame the human for not following directions and not worry about it.

Line 16 lets the human type in something which the Scanner object will attempt to convert into a double value, and line 19 lets the human type in a String. (Anything can be packaged as a String, including numbers, so this isn&rsquo;t likely to fail.)

Try running the program several more times, noticing when it blows up and when it doesn&rsquo;t.