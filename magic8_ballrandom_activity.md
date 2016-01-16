<!--djw: lacks originality-->
###Magic 8 ball random activity
{%ace edit=true, lang='java'%}
import java.util.Random;

public class Magic8Ball
{
	public static void main ( String[] args )
	{
		Random r = new Random();

		int choice = 1 + r.nextInt(15);
		String response = "";

		if ( choice == 1 )
			response = "It is certain";
		else if ( choice == 2 )
			response = "It is decidedly so";
		else if ( choice == 3 )
			response = "Without a doubt";
		else if ( choice == 4 )
			response = "Yes - definitely";
		else if ( choice == 5 )
			response = "You may rely on it";
		else if ( choice == 6 )
			response = "As I see it, yes";
		else if ( choice == 7 )
			response = "Most likely";
		else if ( choice == 8 )
			response = "Outlook good";
		else if ( choice == 9 )
			response = "Signs point to yes";
		else if ( choice == 10 )
			response = "Yes";
		else if ( choice == 11 )
			response = "Reply hazy, try again";
		else if ( choice == 12 )
			response = "Ask again later";
		else if ( choice == 13 )
			response = "Better not tell you now";
		else if ( choice == 14 )
			response = "Cannot predict now";
		else if ( choice == 15 )
			response = "Concentrate and ask again";
		else 
			response = "8-BALL ERROR!";

		System.out.println( "MAGIC 8-BALL SAYS: " + response );
	}
}
{%endace%}
What You Should See

Your answers will probably be different than these. Actually, that's kind of the point.
```
MAGIC 8-BALL SAYS: It is decidedly so
MAGIC 8-BALL SAYS: Reply hazy, try again
MAGIC 8-BALL SAYS: Signs point to yes
```

1. The real Magic 8-Ball™ contains 20 responses, not 15. Change the code so that it picks a random number from 1-20, and add the following five responses:

Don't count on it
My reply is no
My sources say no
Outlook not so good
Very doubtful

2. Next, modify the code above so the Magic8Ball is contained in a class. The class contains a method called shake which generates a random answer. So you implement the Magic8Ball class in your main method as follows:

response = Magic8Ball.shake()

3. Finally, modify the existing console application to prompt the user to ask a question. Then, when the user hits enter, the Magic8Ball class returns a random response. Finally the app asks the user if they want to ask another question. Allow the user to ask as many questions as they like until they decide to quit.

In the main method you should handle all the code that deals with the user interaction such as asking questions and printing responses to the console. However, the Magic8Ball class should handle anything that has to do with the functionality of generating a random response.

 