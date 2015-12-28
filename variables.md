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
At the top of the program we declare the variables. It's common practice to declare variables at the top of your method or class. Variables declared within a method are visible only within that method. 

You want to choose the appropriate data type for your variable. Names are stored as ```String``` variables. Numbers without decimal points are stored as ```int``` variables.

A float uses less memory than a double. Floats should not be used for precise values, such as currency. The ```java.math.BigDecimal``` class is intended for currency values since it is more accurate. We'll look at that later.


####What you should do
1. Copy the above program to Eclipse and be able to generate the same output shown above. 
2. Modify the variables to print your name and age. 
3. Put a space between your first and last names.
4. Add a variable for the last movie you saw. 
5. Add a variable for your GPA. Display that. If you don't like your GPA make one up.