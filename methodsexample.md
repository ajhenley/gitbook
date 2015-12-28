<!--djw: done-->
###Methods example
This is an example of using methods in Java

####For reusable code

If you need to do the same thing, or almost the same thing, many times, write a method to do it, then call the method each time you have to do that task.

####To parameterize code

In addition to making reusable code that is the same in all cases, you will often want to use parameters that change the way the method works.

####For top-down programming

A very useful style of programming is called top-down programming. You solve a big problem (the "top") by breaking it down into little problems. To do this in a program, you write a method for solving your big problem by calling on other methods to solve the smaller parts of the problem. And these methods for solving the simpler problems similarly call on other methods until you get down to simple methods which solve simple problems

####To create conceptual units

Create methods to do something that is one action in your mental view of the problem. This will make it much easier for you to work with your programs.

####To simplify

Because local variables and statements of a method can not been seen from outside the method, they (and their complexity) are hidden from other parts of the program, which prevents accidental errors or confusion.

 
```java
import java.util.*;

public class MethodsExample {

    public static void invalidValue() {
		System.out.println ("You have entered an invalid value.");
		System.out.println ("The program will now exit.");
		System.exit (0);
    }

    public static void validValue() {
		System.out.println ("You have entered an valid value.");
		System.out.println ("Congratulations!");
		System.out.println ("The program will now exit.");
		System.exit (0);
    }

    public static void main (String args[]) {
		Scanner stdin = new Scanner (System.in);
		System.out.println ("Enter a valid int value");
		int value = stdin.nextInt();
		if ( value == 1 )
		    validValue();
		else if ( value == 2 )
		    validValue();
		else if ( value == 3 )
		    invalidValue();
		else if ( value == 4 )
		    invalidValue();
		else
		    validValue();
    }
}
```
