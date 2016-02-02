###Validation made Easy - er
As users input data into your program you suddenly find the need to validate it. After all, if your program is expecting a numeric quantity it wouldn't do to have the user enter a negative number or a 'Q'. That's where validation comes in. You can create your own validation class and display an error message to the user if their input is not valid. We'll want to be sure the user can only enter strings, doubles or integers.

We'll look at two ways to validate incoming data
* Use the Scanner class to ensure you only get a particular type of data
* Write your own class to validate that the data is within a specific range
 

####Using the Scanner class
Here's an example where we use the Scanner class to ensure we get valid data from the user.

The Scanner class contains a wealth of features for validating and parsing data. The code below usesthe Scanner's ```hasNextInt()``` and ```hasNextDouble()``` methods to determine if the user entered the expected data. We *could* throw an exception in the else clause but we choose to exit gracefully.


{%ace edit=true, lang='java'%}
import java.util.Scanner;

public class ValidationMain {

	public static void main(String[] args) {
		Scanner keyboard = new Scanner(System.in);
		
		//Prompt the user to enter the product code, quantity and price
		
		String productCode = "";
		System.out.println("What would you like to order?");
		productCode = keyboard.nextLine();
		
		int quantity = 0;
		System.out.println("How many would you like?");
		if (keyboard.hasNextInt()){
			quantity = keyboard.nextInt();
		}else{
			System.out.println("Please enter a valid quantity");
		}

		double price = 0.0;
		System.out.println("What is the price?");
		if (keyboard.hasNextDouble()){
			price = keyboard.nextDouble();
		}else{
			System.out.println("Please enter a decimal number");
		}

		//print the order summary
		System.out.printf("You have ordered %d %s for a total cost of $%.2f\n",
											quantity,productCode,quantity*price);
	
	}

}
{%endace%}


####Writing your own class

####Your assignment
Sometimes the Scanner class alone doesn't enforce all our business rules. 
Modify the program above. Add a class that ensures the following:
* The product code must be exactly five characters long
* Quantity is between 0 and 100. 
* Price is between 0.0 and 1000.00

The program should continue prompting the user to enter correct data until the user enters valid data.



