<!--djw:done-->
###Output assignment

Change the following application so that it outputs the values of name,age, height and gpa to the console.
{%ace edit=false, lang='java'%}
import java.util.Scanner;

public class SomethingAboutYou
{
	public static void main( String[] args )
	{
		Scanner sc = new Scanner(System.in);

		String firstName;
		int age;
		String height;
		double gpa;

		System.out.print( "What is your first name? " );
		firstName = sc.next();
		
		System.out.print( "How old are you? " );
		age = keyboard.nextInt();

		System.out.print( "How tall are you? " );
		height = keyboard.next();

		System.out.print( "What is your GPA? " );
		gpa = keyboard.nextDouble();

        }
}
{%endace%}


<button class="section" target="section1" show="Sample Answer" hide="Hide Answer"></button>

<!--sec data-title="Answer" data-id="section1" data-show=false ces-->
{%ace edit=false, lang='java'%}
import java.util.Scanner;

public class SomethingAboutYou
{
	public static void main( String[] args )
	{
		Scanner sc = new Scanner(System.in);

		String firstName;
		int age;
		String height;
		double gpa;

		System.out.print( "What is your first name? " );
		firstName = sc.next();
		
		System.out.print( "How old are you? " );
		age = sc.nextInt();

		System.out.print( "How tall are you? " );
		height = sc.next();

		System.out.print( "What is your GPA? " );
		gpa = sc.nextDouble();

		System.out.println("You are " + firstName);
		System.out.println("You are " + age + " years old.");
		System.out.println("Your height is: " + height);
		System.out.print("Your awesome gpa is: " + gpa);
		
		sc.close();
        }
}
{%endace%}
<!--endsec-->