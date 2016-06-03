<!--djw:done-->
###An array to remember
Storing the history of values in a program is a common task. Maintaining an object's history requires the programmer to either write specific code or use a library which supports history logging. Today you're going to write specific code to store the history of a list.

Create a program that prompts for words and saves those words to a variable. The program remembers the history of the variable because the variable is an array. Next use a for loop to print the words to the console in order the user entered them. Print the history whenever the user types the word History, otherwise save the word that is entered.

Type in the names of the last ten presidents in the order they were elected. When you are done enter the word _history_. Your program should display their names starting with the most recent.

For your convenience the names of the last ten presidents are:<br>
Kennedy, Johnson, Nixon, Ford, Carter, Reagan, Bush, Clinton, Bush, Obama


####Sample Answer
```java
import java.util.Scanner;

public class RememberArray {
	static Scanner sc = new Scanner(System.in);
	static int maxItems = 100;
	static String[] memory = new String[maxItems];
	static int currentItems = 0;
	
	public static void main(String[] args)
	{
		getUserInput(); //An Array to Remember
		sortAndDisplay(); //Bonus Basic Java Assignment
		
	}
	
	private static void getUserInput()
	{
		String input = "";
		System.out.println("Type \'history\' to display remembered phrases starting from most recent.");
		System.out.println("Type \'quit\' to stop input.");
		while(!input.equalsIgnoreCase("quit") && currentItems < maxItems)
		{
			System.out.print("Input word or phrase: ");
			input = sc.nextLine();
			if(input.equalsIgnoreCase("history"))
			{
				rememberHistory();
			}
			else if(input.equalsIgnoreCase("quit"))
			{
				System.out.println("You have chosen to end entry.");
			}
			else
			{
				commitToMemory(input);
			}
		}
	}
	
	private static void commitToMemory(String thing)
	{
		memory[currentItems] = thing;
		currentItems++;
	}
	
	private static void rememberHistory()
	{
		for(int i = currentItems - 1; i >= 0; i--)
		{
			System.out.println(memory[i]);
		}
	}
	
	private static void sortAndDisplay()
	{
		String temp = "";
		System.out.println("Alphabetically sorted: ");
		//Sort
		for(int i = 0; i < currentItems - 1; i++)
		{
			for(int j = 1; j < currentItems - i; j++)
			{
				if(memory[j - 1].compareToIgnoreCase(memory[j]) > 0)
				{
					temp = memory[j - 1];
					memory[j - 1] = memory[j];
					memory[j] = temp;
				}
			}
		}
		//Display
		for(int k = 0; k < currentItems; k++)
		{
			System.out.println(memory[k]);
		}
	}
}
```
