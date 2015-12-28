# Variables

Programs would be pretty boring if the only thing you could do was print things on the screen. We would like our programs to be interactive.

Interactivity requires several different concepts working together. Let's go through each one at a time.

**Variables**: If you paid attention in Algebra class you may recall the concept of variables. So an equation like ```2x + 13 = 25``` allows us to find the value of x. What is x? It's a variable that holds a value. Programming languages have variables, too. The concept is the same:
<blockquote>A variable is a name that refers to a memory location that holds a value.</blockquote>

####Variables in Java have four major differences from math variables:
* Variable names can (and should) be more than one letter long
* Variables can hold more than just numbers; they can hold text or any Java data type
* You choose the type of values the variable will hold when declaring the variable
* The value of a variable can (and often will) change. The data type will not change

Let's look at some code! I'm not going to tell you what the name of the file is supposed to be. You'll have to figure it out for yourself. There is only one correct answer and a clue is below.

```java
/* VariousVaribles - a program to teach us about variables
*/
public class VariousVariables
{
    public static void main( String[] args )
    {
        //declare variables here before we use them
        int x, y, answer; //all three variables will be declared as integers
        double temperature;
        float  Temperature; //a float uses less memory than a double
        String firstName, lastName;
        String question = "unknown"; //question is initialized
        
        //assign values to the variables here
        x = 99;
        y = 2147483647; //you could also use the constant Integer.MAX_VALUE
        answer = 42;
        firstName = "James";
        lastName = "Gosling";
        temperature = 98.6;
        Temperature = 32.0f;
          
        //Use the variables here
        System.out.println( "The variable x contains a value of " + x );
        System.out.print( "The value " + y + " is the largest value ");
        System.out.println( "you can store in an integer." );
        System.out.println("The anwser to the question is: " + answer );
        System.out.println("And the question has long since been " + question);
        System.out.println("If you're not sick your temperature is " 
        														+ temperature);
        System.out.println("If you're an ice cube your temperature is " 
        														+ Temperature);
        System.out.println("The variable Temperature is not "
        										 + "the same as  temperature");
        System.out.println("The founder of Java is " + firstName + lastName );
    }
}
```

####What You Should See
```
The variable x contains a value of 99
The value 2147483647 is the largest value you can store in an integer.
The anwser to the question is: 42
And the question has long since been unknown
If you're not sick your temperature is 98.6
If you're an ice cube your temperature is 32.0
The variable Temperature is not the same as  temperature
The founder of Java is JamesGosling

```
At the top of the program we declare the variables. It's common practice to declare variables at the top of your method. The first three are named <em>x</em>, <em>y</em>, and <em>age</em>. All three of these variables are &ldquo;integers&rdquo;, which is the type of variable that can hold a value between &plusmn; two billion.</p>
<p>A variable which is an integer could hold the value 10. It could hold the value <span class="pre">-8192</span>. An integer variable can hold 123456789. It could <em>not</em> hold the value 3.14 because that has a fractional part. An integer variable could <em>not</em> hold the value 10000000000 because ten billion is too big.</p>
<p>On line 6 we declare variables named <em>seconds</em>, <em>e</em>, and <em>checking</em>. These three variables are &ldquo;doubles&rdquo;, which is the type of variable that can hold a number that might have a fractional part.</p>
<p>A variable which is a double could hold the value 4.71. It could hold the value <span class="pre">-8192</span>. (It <em>may</em> have a fractional part but doesn&rsquo;t have to.) It can pretty much hold <em>any</em> value between &plusmn; 1.79769 &times; 10<sup>308</sup> and 4.94065 &times; 10<sup>-324</sup>.</p>
<p>However, doubles have limited precision. Notice that on line 14 I store the value 2.71828182845904523536 into the variable named <em>e</em>, but when I print out that value on line 24, only 2.718281828459045 comes out. Doubles do not have enough significant figures to hold the value 2.71828182845904523536 precisely. Integers have perfect precision, but can only hold whole numbers and can&rsquo;t hold huge huge values.</p>
<p>The last type of variable we are going to look at in this exercise is the String. On line 7 we declare three String variables: <em>firstName</em>, <em>last_name</em> and <em>title</em>. String variables can hold words and phrases; the name is short for &ldquo;string of characters&rdquo;.</p>
<p>On lines 9 through 11 we initialize the three integer values. The value 10 is stored into <em>x</em>. Before this point, the variable <em>x</em> exists, but its value is undefined. 400 is stored into <em>y</em> and 39 is stored into the variable <em>age</em>.</p>
<p>Lines 13 through 15 give initial values to the three double variables, and lines 17 through 19 initialize the three String variables. Then lines 21 through 26 display the values of those variables on the screen. Notice that the variable names are not surrounded by quotes.</p>
<p>I know that it doesn&rsquo;t make sense to use variables for a program like this, but soon everything will become clear.</p>
