<!-- djw:done-->
<!--todo: how many sq yards can he mow in 2 minutes? Does this make sense? -->
Bob has a lawn service business. Bob estimates that he can mow 40 sq yard of lawn in 2 minutes. Write a program that will allow Bob to enter the length and width of a lawn. The program should then compute the square yardage and the time it will take to mow it. Display the length, width, square yardage, and the amount of time to mow it.


<button class="section" target="section1" show="Sample Answer" hide="Hide Answer"></button>

<!--sec data-title="Answer" data-id="section1" data-show=false ces-->
{%ace edit=false, lang='java'%}
import java.util.Scanner;

public class MowingTime
{
  public static void main( String[] args )
  {
    Scanner keyboard = new Scanner(System.in);
    double length, width, lawnArea;

    System.out.print( "Lawn length? " );
    length = keyboard.nextDouble();

    System.out.print( "Lawn width? " );
    width = keyboard.nextDouble();
  
    lawnArea = length * width;

    System.out.println("The are of the lawn is " + lawnArea + " sq yard, and Bob can mow it in "+ (lawnArea * 2) + " minutes.");

    keyboard.close();
  }
}
{%endace%}
<!--endsec-->