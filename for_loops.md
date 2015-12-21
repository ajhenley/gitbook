# Counting with for loops
  
As you have seen in previous exercises, while loops and do-while loops can be used when you want to repeat a set of instructions.

But loops keep going as long as something is true. What if you want to do something a given number of times and you know the number of interations.Then you want a for loop.

```java
import java.util.Scanner;

public class BartsBlackboardAutomator
{
    public static void main( String[] args )
    {
        Scanner keyboard = new Scanner(System.in);

        int n;
        String message;
        //whenever Bart Simpson gets in trouble he has to write something on the blackboard. 
        //Now he can use this program to do it for him..... leaving him more time for trouble!
        System.out.println( "Type in your message, Bart, and I'll display it one hundred times." );
        System.out.print( "Message: " );
        message = keyboard.nextLine();
        
        //Array numbering starts with zero. But we're using a for loop 
        //so we can set the start point and end point to anything we want.
        for ( n = 1 ; n <= 100 ; n++ )
        {
            //The counter variable, n, is within scope inside the loop
            //but not accessible outside the loop
            System.out.println( n + ". " + message );
        }
        // ERROR! n is not visible
        // System.out.println("value of n = " + n);
        
        

    }
}
```
####Notes on for loops
The for loop contains three expressions in the parenthesis following the word ```for``` . 
They are called initialization, ``` n = 1```, condition ```n <= 100```, and update, ```n++```). 

Each could also be missing but you would still need to include the ```;``` anyway. If a condition is missing, it is assumed to be equal to true. If all three were missing you'd have an endless for loop. Which would be the same as a do-loop or a while-loop. To get out of such a loop you would need a terminating condition in the body that broke out with the keyword ```break```.


####Recommendations
* Use the three parts of the for loop according to their intended meaning described above, and with reference to a control variable for the loop
* Do not modify the control variable in the body of the loop

####Your assignment
Use a for loop and a method to print the lyrics to 99 Bottles of Beer on the Wall. It is not necessary for you to sing out loud.