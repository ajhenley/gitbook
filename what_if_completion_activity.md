<!--djw:done-->
###What if completion activity

Start with the code below and create a program that will output the sum, product and average of num1 and num2. If the calculated sum is over 200, print an asterisk next to the sum.

{%ace edit=false, lang='java'%}
import java.util.Scanner;

public class PairProcess {
	public static void main(String[] args) {
		int num1, num2;
		
		Scanner keyboard = new Scanner(System.in);
		
		System.out.print( "First Number? :" );
		num1 = keyboard.nextInt();
		
		System.out.print( "Last Number?  :" );
		num2 = keyboard.nextInt();

		
	}
}
{%endace%}

Bonus If the calculated sum is under 1000 it should have a tilde ~ printed next to it.

<button class="section" target="section1" show="Sample Answer" hide="Hide Answer"></button>

<!--sec data-title="Answer" data-id="section1" data-show=false ces-->
{%ace edit=false, lang='java'%}
public class HelloWorld
 {
    public static void main( String[] args )
    {
        System.out.println( "Hello, World!" );
        System.out.println("Today is July 19, 2015. I am alive!");
        System.out.println("My name is Alton.");
    }
 }
{%endace%}
<!--endsec-->

<button class="section" target="section2" show="Sample Bonus Answer" hide="Hide Answer"></button>

<!--sec data-title="Answer" data-id="section2" data-show=false ces-->
{%ace edit=false, lang='java'%}
public class HelloWorld
 {
    public static void main( String[] args )
    {
        System.out.println( "Hello, World!" );
        System.out.println("Today is July 19, 2015. I am alive!");
        System.out.println("My name is Alton.");
    }
 }
{%endace%}
<!--endsec-->