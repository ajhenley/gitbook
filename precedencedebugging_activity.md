###Precedence Debugging Activity

The following code is trying to do math with strings. Can you fix this code to make it work?

{%ace edit=true, lang='java'%}
import java.util.Scanner;

public class CastingDebuggingActivity {
	public static void main(String[] args) {
		Scanner cookie = new Scanner(System.in);
		String input;
		int accumulator = 0;
		
		System.out.print("Gimme a number :");
		input = cookie.next();
		while (input != "")
		{
			accumulator += input;
			
			System.out.println(" running total => " + accumulator);
			System.out.print("Next number : ");
			input = cookie.next();
		}
	}
}
{%endace%}

What You Should See

```
Gimme a number :9
 running total => 9
Next number : 78
 running total => 87
Next number : 123
 running total => 210
Next number : -209
 running total => 1
Next number : 
```