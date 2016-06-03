<!--djw:done-->
<!--ajh:done-->
###What if activity

Create a program that allows the user enter a sales record (which includes customer number, name, sales amount and a tax code).

|tax code|tax amount|
|-|-|
|NRM|6%|
|NPF|0%|
|BIZ|4.5%|
 

The program should output a total that includes the tax owed (if any).
```java
import java.util.Scanner;

public class SalesRecord {
	public static void main(String[] args) {
		String custnum, name, taxcode;
		double salesamt;
		
		Scanner keyboard = new Scanner(System.in);
		
		System.out.print("Customer Number : ");
		custnum = keyboard.next();
		
		System.out.print("Name : ");
		name = keyboard.next();
		
		System.out.print("Sales amount : $");
		salesamt = keyboard.nextDouble();
		
		System.out.print("Tax Code : ");
		taxcode = keyboard.next();
		
		if (taxcode.equals("NRM"))
			System.out.println("Total (with tax) : $" + (salesamt * 1.06));
		else if (taxcode.equals("NPF"))
			System.out.println("Total (with tax) : $" + (salesamt * 1));
		else if (taxcode.equals("BIZ"))
			System.out.println("Total (with tax) : $" + (salesamt * 1.04555));
	}
}
```