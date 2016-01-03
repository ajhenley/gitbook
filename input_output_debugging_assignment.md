<!--djw:done-->
###Input output debugging assignment

This application takes three numbers adds them together and outputs the result, or at least it should, can you fix it?
{%ace edit=false, lang='java'%}
import java.util.Scanner;

public class AskingQuestions
{
	public static void main( String[] args )
	{
		Scanner keyboard = new Scanner(System.in);

		double num1, num2, num3;

		System.out.print( "First integer? " );
		num1 = keyboard.nextString();

		System.out.print( "Second integer? " );
		num2 = keyboard.nextInt();

		System.out.print( "Third integer? " );
		num3 = keyboard.nextDouble();
    }
        System.out.println("The total is : " + (num1 + num2 + num3));
    }
{%endace%}


<button class="section" target="section1" show="Sample Answer" hide="Hide Answer"></button>

<!--sec data-title="Answer" data-id="section1" data-show=false ces-->
{%ace edit=false, lang='java'%}
import java.util.Scanner;

public class AskingQuestions
{
	public static void main( String[] args )
	{
		Scanner keyboard = new Scanner(System.in);

		int num1, num2, num3;

		System.out.print( "First integer? " );
		num1 = keyboard.nextInt();

		System.out.print( "Second integer? " );
		num2 = keyboard.nextInt();

		System.out.print( "Third integer? " );
		num3 = keyboard.nextInt();
		
		System.out.println("The total is : " + (num1 + num2 + num3));
    }
}
{%endace%}
<!--endsec-->