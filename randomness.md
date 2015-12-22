# Randomness
<!--redo: Create a random password with one of five formats-->


You know what's cool? Having the computer randomly choose a number. This is the basis of pretty much every computer game ever.
To pick a random number, you first need to import ```java.util.Random;```
Then, you must create a random-number generator object, like so:

```Random rnd = new Random();```
Once that's finished, you can have the computer pick a random integer like this:

```int x = 1 + rnd.nextInt(100);```That'll pick a random number from 1 to 100 (inclusive) and store it into the variable x. Let's look at some code!

```java
import java.util.Random;

public class RandomGenerator{

    public static void main(String []args)
    {
        output("Generate 10 random integers between 0 and 99");

        Random rnd = new Random();
        
        for (int i = 1; i <= 10; ++i)
        {
          int randomInt = 1 + rnd.nextInt(100);
          output("Generated number: " + randomInt);
        }
    
        output("Done.");
    }
  
  private static void output(String aMessage)
  {
    System.out.println(aMessage);
  }
}
```

1. Delete the 1 + in front of all six lines that pick numbers 1-5, so that they look like this: System.out.print( r.nextInt(5) + " " ); Run the program a few times, and see if you can figure out what range the new random numbers are in.
2. Change the 1 + in front of all six lines that pick numbers 1-5, so that they look like this: System.out.print( 3 + r.nextInt(5) + " " ); Run the program a few times. Is it picking random numbers from 3 to 5? If not, what range are they?
3. Change the line where you create the random number generator so that it looks like this: Random r = new Random(12353); This number is called a seed. Run the program a few times. What do you notice? What happened to the random numbers?
4. Change to random seed to something else and observe the behavior. What happens to the random numbers?
5. (Delete the random seed before turning in the assignment.)