<!--djw:done-->
###Finally Clause Assignment
Add the following Finally clause to the previous application. Run your program with an exception. Run it again without an exception.

```java
finally {
    System.out.println("finally block will execute.");
}
```

```java
import java.util.Scanner;

class Division {
	public static void main(String[] args) {

		int a, b, result;

		Scanner input = new Scanner(System.in);
		System.out.println("Input two integers");

		a = input.nextInt();
		b = input.nextInt();
		try
		{
			result = a / b;
			System.out.println("Result = " + result);
		}
		catch(ArithmeticException e)
		{
			System.out.println("You cannot divide by zero.");
		}
		finally
		{
			System.out.println("finally block will execute");
		}
	}
}
```