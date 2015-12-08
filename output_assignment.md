# Output assignment

Change the following application so that it outputs the values of age, height and gpa to the console.
```
import java.util.Scanner;

public class AskingQuestions
{
	public static void main( String[] args )
	{
		Scanner keyboard = new Scanner(System.in);

		int age;
		String height;
		double gpa;

		System.out.print( "How old are you? " );
		age = keyboard.nextInt();

		System.out.print( "How tall are you? " );
		height = keyboard.next();

		System.out.print( "What is your GPA? " );
		gpa = keyboard.nextDouble();

        }
}```