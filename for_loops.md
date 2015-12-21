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
            System.out.println( n + ". " + message );
        }

    }
}
```