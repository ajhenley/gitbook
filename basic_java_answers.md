# Basic Java Answers

## Your first java program

```java
public class HelloWorld
 {
    public static void main( String[] args )
    {
        System.out.println( "Hello, World!" );
        System.out.println("Today is July 19, 2015. I am alive!");
        System.out.println("My name is Alton.");
    }
 }
```


## More Printing

```java
public class PrintReceipt
{
  public static void main( String[] args )
  {
      System.out.println( "+--------------------------------------+");
      System.out.println( "|      Java Bank ATM Receipt           |");
      System.out.println( "|      Wednesday, December 2, 2015     |");
      System.out.println( "|      ATM Location # 123              |");
      System.out.println( "|                                      |");
      System.out.println( "|                                      |");
      System.out.println( "|      Account Number:      1234567    |");
      System.out.println( "|      Customer:     John Q. Public    |");
      System.out.println( "|      Transaction Type:    Deposit    |");
      System.out.println( "|      Transaction Amount:  $500.00    |");
      System.out.println( "|      Account Balance:   $1,500.00    |");
      System.out.println( "|                                      |");
      System.out.println( "|      Thank you for banking with us   |");
      System.out.println( "|            Have a coffee day         |");
      System.out.println( "|                                      |");
      System.out.println( "+--------------------------------------+");
  }
}
```


## A program for yourself

```java
public class MyProgram
 {
    public static void main( String[] args )
    {
        // My name is Alton
        // I am 47 years old
    }
 }
```


## Debug this program

```java
public class DebugProg {
    public static void main(String[] args) {
        double x, y;

        x = 3.1415;
        y = 3.64;

        System.out.println("pi is approximately " + x);
        System.out.println("My GPA was " + y);
    }
}
```


##Math two

```java
public class MathTwoProg {
    public static void main(String[] args) {
        int myNumber;
        double myOtherNumber;

        myNumber = 2;
        myOtherNumber = 1.7938;

        System.out.println("myNumber is " + myNumber);
        System.out.println("myOtherNumber is " + myOtherNumber);
    }
}
```


##Change Program
```java
public class ChangeProgram {
    public static void main(String[] args) {
        int x;
        double y, z;

        x = 5;
        y = 8.75;

        z = x * y;

        System.out.println("The product is " + z);
    }
}
```


##Getting and Storing User Input
```java
import java.util.Scanner;

public class GettingInput {
	public static void main(String[] args) {
		Scanner keyboard = new Scanner(System.in);
		
		String firstInitial = keyboard.next();
		String lastName = keyboard.next();
		int houseNumber = keyboard.nextInt();
		String streetName = keyboard.next();
		String streetType = keyboard.next();
		String city = keyboard.next();
		
		System.out.print(firstInitial + " " + lastName + " " + houseNumber + " ");
		System.out.println(streetName + " " + streetType + " " + city);
	}
}
```


##String Completion Assignment
```java
import java.util.Scanner;

public class PetQuestions {
	public static void main(String[] args) {
        String name;
        String breed;
        int age;

        Scanner keyboard = new Scanner(System.in);
        
        System.out.print( "Greetings. What is your pet's name? " );
        name = keyboard.next();
 
        System.out.print( "What kind of animal is " + name + "? " );
        breed =keyboard.next();
        
        System.out.print( "How old is " + name + "? ");
        age = keyboard.nextInt();
        
        System.out.println( name + " is your " + breed + " and it is " + age );
	}
}
```


##String Assignment
```java
public class StringAssignment {
	public static void main(String[] args) {
		String name = "Alton";
		System.out.print(name);
	}
}
```


##Special Characters Assignment

```java
public class SpecialCharacters {
	public static void main(String[] args) {
	    String message1, message2;

	    message1 ="message1 = \\/\\/\\/\\/\\/\\r\\t\\b ";
	    message2 = "\nmessage2 = \";";

	    System.out.println(message1 + message2);
	}
}
```

Need it explained? Then watch the video walkthrough...<br />
[Video Walkthrough - http://links.learningbycoding.com/specialchars](https://ajhenley.wistia.com/medias/hgvfnibluf)


##Output Assignment

```java
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
```

##Input Output Debugging Assignment

```java
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
```


##Input Output Change Assignment

```java
import java.util.Scanner;

public class AskingQuestions
{
	public static void main( String[] args )
		Scanner keyboard = new Scanner(System.in);

		int num1, num2, num3;

		System.out.print( "First temperature? " );
		num1 = keyboard.nextInt();

		System.out.print( "Second temperature? " );
		num2 = keyboard.nextInt();

        System.out.println("The max value is : " + (num1 + num2) / 2);
    }
}
```


#Mowing Time Programming Activity

```java
import java.util.Scanner;

public class MowingTime
{
  public static void main( String[] args )
  {
    Scanner keyboard = new Scanner(System.in);
    double length, width, lawnArea;

    System.out.print( "Lawn length? " );
    length = keyboard.nextDouble();

    System.out.print( "Lawn width? " );
    width = keyboard.nextDouble();
  
    lawnArea = length * width;

    System.out.println("The are of the lawn is " + lawnArea + 
      " sq yard, and Bob can mow it in "+ (lawnArea / 40 * 2) + 
      " minutes.");

    keyboard.close();
  }
}
```


##More Mowing Time

```java
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
		lawnTimeHrs= (lawnArea / 40 * lawnTimeRate) / 60;

		System.out.println("The area of the lawn that needs to be mowed is " 
          + lawnArea + " sq yar. It will take "+ lawnTimeHrs + 
          " hours to finish the mowing and will cost " + 
          currency.format((float)(lawnTimeHrs * lawnCostRate)) + ".");
          
		System.out.println("If Bob charges $45 per lawn, " + 
          "then the profit will be: " + 
          currency.format((float)(45 - lawnTimeHrs * 45)));
          
		keyboard.close();
    }
}
```


##What If Change Activity

```java
import java.util.Scanner;

public class StudentRecordReader {
	public static void main(String[] args) {
		String fname, lname, status;
		double gpa;
		int hours;
	
		Scanner keyboard = new Scanner(System.in);
	
		System.out.print( "Student's First Name? " );
		fname = keyboard.next();
	
		System.out.print( "Student's Last Name? " );
		lname = keyboard.next();
	
		System.out.print( "Student's GPA? " );
		gpa = keyboard.nextDouble();
	
		System.out.print( "Student's Current Course Load? " );
		hours = keyboard.nextInt();
	
		if (hours >= 12)
		{
			System.out.println();
			System.out.println("Student Name :" + fname + " " + lname);
			System.out.println("Student GPA :" + gpa);
			if (gpa >= 3)
			{
				System.out.println("This student is in good standing.");
			} else if (gpa >= 2)
			{
				System.out.println("This student needs to study more.");
			} else if (gpa >= 1)
			{
				System.out.println("This student is on academic probation.");
			} else
			{
				System.out.println("This student has been expelled.");
			}
		}
	}
}
```


##What if debugging activity

```java
import java.util.Scanner;

public class StudentRecordReader {

	public static void main(String[] args) {
		String fname, lname;
		double gpa;
		
		Scanner keyboard = new Scanner(System.in);
		
		System.out.print( "Student's First Name? " );
		fname = keyboard.next();
		
		System.out.print( "Student's Last Name? " );
		lname = keyboard.next();

		System.out.print( "Student's GPA? " );
		gpa = keyboard.nextDouble();
		
		System.out.println();
		System.out.println("Student Name :" + fname + " " + lname);
		System.out.println("Student GPA :" + gpa);
		if (gpa >= 3)
		{
			System.out.println("This student is in good standing.");
		} else if (gpa >= 1)
		{
			System.out.println("This student is on academic probation.");
		} else
		{
			System.out.println("This student has been expelled.");
		}
	}
}
```
