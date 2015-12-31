<!--djw:done-->
###Repeating yourself with the while loop
You are going to learn how to make sections of your code repeat. This will give you the ability to reuse your code so you don't have to write the same code multiple times.

{%ace edit=true, lang='java'%}
import java.util.Scanner;

public class KeepGuessing {
	public static void main(String[] args) {
		Scanner keyboard = new Scanner(System.in);
		int secretNumber,guess;
		
		secretNumber = 123;
		
		System.out.println("I'm thinking of a number between 1 and 1000");
		System.out.print("Enter the number:");
		guess = keyboard.nextInt();
		
		while ( guess != secretNumber )
		{
			System.out.println("\nYou are wrong. Try again.");
			System.out.println("Enter the number: ");
			guess = keyboard.nextInt();
		}
		
		System.out.println("You are correct. You win a prize!");
		keyboard.close();
	}
}
{%endace%}


####Your assignment
The while loop will continue until the test condition is true. You can also break out of a while loop by using the keyword ```break```. Modify the above program to exit the while loop after 5 guesses.

