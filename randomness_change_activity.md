<!--ajh:done-->

# Randomness change activity

The following code, our program from last time, generates a random number between 1 and 6, inclusive. Change the code to generate a random integer between 5 and 95.

{%ace edit=false, lang='java'%}
import java.util.Random;

public class RandomGenerator{
    public static void main(String[] args)
    {
        output("Generate 10 random integers between 1 and 6");

        Random rnd = new Random();
        
        for (int i = 1; i <= 10; ++i)
        {
          int randomInt = 1 + rnd.nextInt(6);
          System.out.println("Generated number: " + randomInt);
        }
    
        System.out.println("Done.");
    }
}
{%endace%}




<button class="section" target="section1" show="Sample Answer" hide="Hide Answer"></button>

<!--sec data-title="Answer" data-id="section1" data-show=false ces-->
{%ace edit=false, lang='java'%}
import java.util.Random;

public class RandomGenerator{
    public static void main(String[] args)
    {
        System.out.println("Generate 10 random integers between 5 and 95");

        Random rnd = new Random();
        
        for (int i = 1; i <= 10; ++i)
        {
          int randomInt = 5 + rnd.nextInt(91);
          System.out.println("Generated number: " + randomInt);
        }
    
        System.out.println("Done.");
    }
}
{%endace%}
<!--endsec-->