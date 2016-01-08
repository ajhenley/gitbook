<!--ajh:done-->
# Randomness debugging activity

This program should generate 10 random integers from 1 to 6. Fix it so that it works...

{%ace edit=false, lang='java'%}
import java.util.random;

public class RandomGenerator{
    public static void main(String[] args)
    {
        output("Generate 10 random integers between 0 and 6");
        Random rnd;
        
        for (int i = 1; i <= 12; ++i)
        {
          int randomInt = 1 + rnd.nextInt(0 to 6);
          output("Generated number: " + randomInt);
        }
    
        output("Done.");
    }
  
  private static void output(String aMessage)
  {
    System.out.println(aMessage);
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
        output("Generate 10 random integers between 1 and 6");

        Random rnd = new Random();
        
        for (int i = 1; i <= 10; ++i)
        {
          int randomInt = 1 + rnd.nextInt(6);
          output("Generated number: " + randomInt);
        }
    
        output("Done.");
    }
  
  private static void output(String aMessage)
  {
    System.out.println(aMessage);
  }
}
{%endace%}
<!--endsec-->