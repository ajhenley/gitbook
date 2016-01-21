<!--djw:used to be Magic 8 ball-->
###Random fortune activity
Most of the life of a program is spent in maintenance. For that reason, most of the life of a programmer is spent maintaining and modifying previously developed programs.

Your job now is to modify the following application. The first step is to copy the code to Eclipse and get it running. You'll see that the program simply prints out a fortune and then exits.

There aren't enough fortunes. Add five more. You can make them up or you can search online for ideas. Change the code so that it picks a random number from 1-20 and add your fortunes.

We'd like to apply what we know about classes to minimize the code in main() and take advantage of object-oriented design. You should create a class called Fortune which simply returns a random fortune. The class shall contain a method which generates a random fortune. Implement the Fortune class in your main method as follows:

```response = Fortune.breakCookie();```

We've already learned about while loops. A while loop would to allow the user to receive another  fortune or exit. Add a while loop to the program so the user is continally prompted to either get a fortune or exit.


{%ace edit=true, lang='java'%}
import java.util.Random;

public class Fortune
{
	public static void main ( String[] args )
	{
		Random r = new Random();

		int choice = 1 + r.nextInt(15);
		String response = "";

		if ( choice == 1 )
			response = "Your smile brings happiness to everyone you meet.";
		else if ( choice == 2 )
			response = "A smile is your passport into the hearts of others.";
		else if ( choice == 3 )
			response = "Hard work pays off in the future, laziness pays off now.";
		else if ( choice == 4 )
			response = "If you have something good in your life, don't let it go!";
		else if ( choice == 5 )
			response = "You learn from your mistakes... You will learn a lot today.";
		else if ( choice == 6 )
			response = "You will travel to many exotic places in your lifetime.";
		else if ( choice == 7 )
			response = "Your wish will come true.";
		else if ( choice == 8 )
			response = "Its amazing how much good you can do if you don't care who gets the credit.";
		else if ( choice == 9 )
			response = "Bloom where you are planted.";
		else if ( choice == 10 )
			response = "All the water in the world can't sink a ship unless it gets inside.";
		else if ( choice == 11 )
			response = "A winner never cheats and a cheater never wins.";
		else if ( choice == 12 )
			response = "Never miss a chance to keep your mouth shut.";
		else if ( choice == 13 )
			response = "Choose a job you love, and you will never have to work a day in your life.";
		else if ( choice == 14 )
			response = "Wherever you go, go with all your heart.";
		else if ( choice == 15 )
			response = "Silence is a true friend who never betrays.";
		else 
			response = "To know what you know and what you do not know, that is true knowledge.";

		System.out.println( "Your fortune says: " + response );
	}
}
{%endace%}




 