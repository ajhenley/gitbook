<!--ajh:done-->
Complete the following program so that it creates a random die roll (random numbers from 1 to 6).
# Randomness completion activity
{%ace edit=false, lang='java'%}
import java.

public class DiceRoller
 {
    public static void main( String[] args )
    {
        int dienumber;
        Random rnd =
        
        dienumber = 
        
        System.out.println("Your die roll was : " + dienumber);
    }
 }
{%endace%}



<button class="section" target="section1" show="Sample Answer" hide="Hide Answer"></button>

<!--sec data-title="Answer" data-id="section1" data-show=false ces-->
{%ace edit=false, lang='java'%}
import java.util.Random;

public class DiceRoller
 {
    public static void main( String[] args )
    {
        int dienumber;
        Random rnd = new Random();
        
        dienumber = 1 +rnd.nextInt(6);
        
        System.out.println("Your die roll was : " + dienumber);
    }
 }
{%endace%}
<!--endsec-->