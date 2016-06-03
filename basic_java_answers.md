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