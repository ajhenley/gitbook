<!--djw:done-->
###Bonus assignment

In this assignment you will write a program to implement the bubble sort. We saw the bubble sort in the algorithm's section but here is the pseudo code for it. Your task is to prompt the user for a word. Use the last names of the presidents. Save the list to a file. Next, read the file into an array and use the bubble sort algorithm to sort the file. Finally, print the sorted file to the screen.


####Bubble sort algorithm
``` 
    For i = 0 to n - 1
        For j = 1 to n - 1
            If (a(j) > a(j + 1))
                temp = a(j)
                a(j) = a(j + 1)
                a(j + 1) = temp
            End-If
        End-For
    End-For
```

The Presidents (since Kennedy) by last name:
* Kennedy
* Johnson
* Nixon
* Ford
* Carter
* Reagan
* Bush
* Clinton
* Bush
* Obama
 
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
