<!-- djw:done-->
<!--ajh:done-->
# More mowing time

Bob realized that his estimates are incorrect. He forgot to account for the house on the yard. Also, he wants to know what it costs to mow each lawn. Assume Bob's clients have rectangular houses and rectangular yards. It's a well-planned community. Prompt for the length and width of the house and remove that from your estimate. Also, assume that Bob pays Joe $12.00 per hour. How much does it cost to mow the lawn? How much does Bob make if he charges $45.00 per lawn?

Modify the mowing time program to allow Bob to enter the length and width of a lawn, the length and width of the house and compute the square yardage and the time it will take to mow it. Also compute the cost to mow the yard.

Print the result of the cost calculation using the number formatter so it shows as a currency. 



<button class="section" target="section1" show="Sample Answer" hide="Hide Answer"></button>

<!--sec data-title="Answer" data-id="section1" data-show=false ces-->
{%ace edit=false, lang='java'%}
import java.text.NumberFormat;
import java.util.Scanner;

public class MowingAssignment
{
	public static void main( String[] args )
	{
		Scanner keyboard = new Scanner(System.in);
		NumberFormat currency = NumberFormat.getCurrencyInstance();

		//keep the rates as constants to make updates and changes easier
		final int lawnTimeRate= 2;
		final int lawnCostRate = 12 ;

		double yardLength, yardWidth, houseLength, houseWidth, lawnArea, lawnTimeHrs;

		System.out.print( "What is the yard length? " );
		yardLength = keyboard.nextDouble();

		System.out.print( "What is the yard width?" );
		yardWidth = keyboard.nextDouble();

		System.out.print( "What is the house length? " );
		houseLength = keyboard.nextDouble();

		System.out.print( "What is the yard width?" );
		houseWidth = keyboard.nextDouble();

		lawnArea = (yardLength * yardWidth) - (houseLength * houseWidth); 

		//convert time from minutes to hours 
		lawnTimeHrs= (lawnArea * lawnTimeRate) / 60;

		System.out.println("The area of the lawn that needs to be mowed is " + lawnArea + " sq yar. It will take "+ lawnTimeHrs + 
		" hours to finish the mowing and will cost " + currency.format((float)(lawnTimeHrs * lawnCostRate)) + ".");
		System.out.println("If Bob charges $45 per hour, then the new cost will be: " + currency.format((float)(lawnTimeHrs * 45)));
		keyboard.close();
    }
}
{%endace%}
<!--endsec-->