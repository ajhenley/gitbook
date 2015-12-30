###Repeating yourself with the while loop
You are going to learn how to make sections of your code repeat. This will give you 


<pre>import java.util.Scanner;

public class EnterPIN {
	public static void main(String[] args) {
		Scanner keyboard = new Scanner(System.in);
		int pin, entry;
		
		pin = 12345;
		
		System.out.println("Welcome to the bank of Java");
		System.out.print("ENTER YOUR PIN:");
		entry = keyboard.nextInt();
		
		while ( entry != pin )
		{
			System.out.println("\nINCORRECT PIN. TRY AGAIN.");
			System.out.println("ENTER YOUR PIN: ");
			entry = keyboard.nextInt();
		}
		
		System.out.println("\nPIN ACCEPTED. YOU NOW HAVE ACCESS TO YOUR ACCOUNT.");
	}
}
</pre>
<h2>What you should see</h2>
<pre>Welcome to the bank of Java
ENTER YOUR PIN:123

INCORRECT PIN. TRY AGAIN.
ENTER YOUR PIN: 
1234

INCORRECT PIN. TRY AGAIN.
ENTER YOUR PIN: 
12345

PIN ACCEPTED. YOU NOW HAVE ACCESS TO YOUR ACCOUNT.
</pre>
<p>On line 16 you get your first look at the while loop. A while loop is similar to an if statement. They
both have a condition in parentheses that is checked to see if it true or false. If the condition is false,
both while loops and if statements will skip all the code in the body. And when the condition is true,
both while loops and if statement will execute all of the code inside their body one time.</p>
<p>The only difference is that if statements that are true will execute all of the code in the curly braces
exactly once. while loops that are true will execute all of the code in the curly braces once and then go
back up and check the condition again. If the condition is still true, the code in the body will all be
executed again. Then it checks the condition again and runs the body again if the condition is still true.</p>
<p>In fact, you could say that the while loop executes all of the code in its body over and over again as
long as its condition is true when checked.</p>
<p>Eventually, the condition will be false when it is checked. Then the while loop will skip over all the
code in its body and the rest of the program will continue. Once the condition of a while loop is false,
it doesn’t get checked again.</p>
<p>Looping is so great because we can finally do something more than once without having to type the code
for it more than once! In fact, programmers sometimes say “Keep your code D.R.Y: Don’t Repeat
Yourself.” Once you know how to program pretty well and finish all of the exercises in this book, you
will start to get suspicious if you find yourself typing (or copyingandpasting) the exact same code
more than once in a program.</p>
  
</div>