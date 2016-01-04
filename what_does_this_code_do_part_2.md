<!--
Original program is below:
import java.util.Scanner;

public class Mortgage {
	
	public static void main(String[] args) {
		
		Scanner keyboard = new Scanner(System.in);
		double loan = 0;
		double interestRate = 0;
		double monthlyPayment = 0;
		double balance = 0;
		int compoundPeriod = 0;
		int term;
		
		System.out.printf("Enter the loan amount: ");
		loan = keyboard.nextDouble();
		
		System.out.printf("Enter the interest rate on the loan: ");
		interestRate = keyboard.nextDouble();
		
		System.out.printf("Enter the term(years) for the loan payment: ");
		term = keyboard.nextInt();
		
		System.out.printf("\n================================================================\n");
		keyboard.close();

		monthlyPayment = getMonthlyPayment(loan, interestRate, term);
		balance = -(monthlyPayment * (term * 12));
		System.out.format("%-30s$%-+10.2f%n", "Amount owed to bank:", balance);
		System.out.format("%-30s$%-10.2f%n", "Minimum monthly payment:", monthlyPayment);
	}

	/**
	 * Calculate the monthly payment of a loan.
	 * 
	 * @param loan Amount borrowed
	 * @param interestRate Interest rate on the loan
	 * @param term Repayment term in years 
	 * @return The monthly payment of a loan given interest rate, amount and term 
	 */
	public static double getMonthlyPayment(double loan, double interestRate, double term) {
		double rate = (interestRate / 100) / 12;
		double base = (rate + 1);
		double months = term * 12;
		double result = 0;
		result = loan * (rate * (Math.pow(base, months)) / ((Math.pow(base, months)) - 1)); 
		
		return result;
	}
}


-->
###What does this code do? Part 2

This code is poorly commented. Actually, it has no comments at all. To make matters worse, the variables are not appropriately named. Can you figure out what this program actually does? Would you like to be the person who is assigned the task of maintaining code like this?

####Your assignment
Clean up the following code by adding comments where appropriate. Also, rename variables and methods to be meaningful and consistent.


{%ace edit=true, lang='java'%}
import java.util.Scanner;

public class Calculator {
	
	public static void main(String[] args) {
		
		Scanner k = new Scanner(System.in);
		double l = 0;
		double i = 0;
		double mp = 0;
		double b = 0;
		int cp = 0;
		int trm;
		
		System.out.printf("Enter the loan amount: ");
		l = keyboard.nextDouble();
		
		System.out.printf("Enter the interest rate on the loan: ");
		i = keyboard.nextDouble();
		
		System.out.printf("Enter the term(years) for the loan payment: ");
		trm = keyboard.nextInt();
		
		System.out.printf("\n================================================================\n");
		keyboard.close();

		mp = getMonthlyPayment(l, i, trm);
		b = -(mp * (trm * 12));
		System.out.format("%-30s$%-+10.2f%n", "Amount owed to bank:", balance);
		System.out.format("%-30s$%-10.2f%n", "Minimum monthly payment:", monthlyPayment);
	}

	public static double getMonthlyPayment(double l, double i, int trm) {
		double rate = (i / 100) / 12;
		double base = (rate + 1);
		int months = trm * 12;
		double result = 0.0;
		result = l * (rate * (Math.pow(base, months)) / ((Math.pow(base, months)) - 1)); 
		
		return result;
	}
}

{%endace%}