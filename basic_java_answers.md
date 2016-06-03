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