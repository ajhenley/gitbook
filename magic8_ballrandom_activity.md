<!--djw:done-->
<!-- used to be Magic 8 Ball but I was inspired to make something more original-->
###Random fortune activity
Most of the life of a program is spent in maintenance. Consequently, most of the life of a programmer is spent maintaining existing programs. 

Your job now is to change the following application. The first step is to copy the code to Eclipse and get it running. You'll see that the program asks the user for their goal and prints out a motivational response. Then it exits.

There aren't enough responses. Add five more. You can make them up or you can search online for ideas. Change the code so that it picks a random number from 1-20 and add your responses.

We'd like to apply what we know about classes to reduce the code in ```main()```. Then we can take advantage of object-oriented design. You should create a class called DeepThoughts which simply returns a random inspirational quote. The class needs a method to generates the random quote. Implement the DeepThoughts class in your main method as follows:

```response = DeepThoughts.inspireMe();```

We've already learned about while loops. A while loop would to allow the user to receive another  quote or exit. Add a while loop to the program so the user is continually prompted to either get a quote or exit. That way the user could have lots of goals.


{%ace edit=true, lang='java'%}
import java.util.Random;
import java.util.Scanner;

public class Inspiration
{
	public static void main ( String[] args )
	{
		Random r = new Random();
		String response = "";

		Scanner keyboard = new Scanner(System.in);
		System.out.println("What is your career goal?");
		String goal = keyboard.nextLine();
		keyboard.close(); //closing the keyboard frees the resource
		
		//choose a random value between 1 and 15
		int choice = 1 + r.nextInt(15);
		
		if ( choice == 1 )
			response = "the man who goes farthest is generally the one who is willing to do and dare.  The sure-thing boat never gets far from shore.";
		else if ( choice == 2 )
			response = "obstacles are those frightful things you see when you take your eyes off your goal.";
		else if ( choice == 3 )
			response = "hard work pays off in the future, laziness pays off now.";
		else if ( choice == 4 )
			response = "what may be done at any time will be done at no time.";
		else if ( choice == 5 )
			response = "you learn from your mistakes... You will learn a lot today.";
		else if ( choice == 6 )
			response = "you will travel to many exotic places in your lifetime.";
		else if ( choice == 7 )
			response = "there are no secrets to success. It is the result of preparation, hard work, and learning from failure.";
		else if ( choice == 8 )
			response = "its amazing how much good you can do if you don't care who gets the credit.";
		else if ( choice == 9 )
			response = "you should bloom where you are planted.";
		else if ( choice == 10 )
			response = "all the water in the world can't sink a ship unless it gets inside.";
		else if ( choice == 11 )
			response = "a winner never cheats and a cheater never wins.";
		else if ( choice == 12 )
			response = "people do not lack strength, they lack will.";
		else if ( choice == 13 )
			response = "you may be disappointed if you fail, but you are doomed if you don’t try.";
		else if ( choice == 14 )
			response = "";
		else if ( choice == 15 )
			response = "no one is wise by birth.  Wisdom results from one’s own efforts.";
		else 
			response = "true knowledge is to know what you know and what you do not know.";

		System.out.println( "Good luck with your goal: " + goal +".");
		System.out.println("It has been said that " + response);
	}
}
{%endace%}




 