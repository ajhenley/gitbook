# What if

Here is the next Java program you'll enter, which introduces you to the if statement. Type this in, make it run exactly right and then we'll see if your practice has paid off.
```
public class WhatIf
{
	public static void main( String[] args )
	{
		int people = 20;
		int cats = 30;
		int dogs = 15;

		if ( people < cats )
		{
			System.out.println( "Too many cats!  The world is doomed!" );
		}

		if ( people > cats )
		{
			System.out.println( "Not many cats!  The world is saved!" );
		}

		if ( people < dogs )
		{
			System.out.println( "The world is drooled on!" );
		}

		if ( people > dogs )
		{
			System.out.println( "The world is dry!" );
		}

		dogs += 5;

		if ( people >= dogs )
		{
			System.out.println( "People are greater than or equal to dogs." );
		}

		if ( people <= dogs )
		{
			System.out.println( "People are less than or equal to dogs." );
		}

		if ( people == dogs )
		{
			System.out.println( "People are dogs." );
		}
	}
}```
What You Should See
```
Too many cats! The world is doomed!
The world is dry!
People are greater than equal to dogs.
People are less than equal to dogs.
People are dogs.
```

###What You Should Do on Your Own
Assignments turned in without these things will receive half credit or less.

In this section, you're going to try to guess what you think the if statement is and what it does.

1. What do you think the if does to the code under it? 
Put your answer in a comment in the code.
2. What is the purpose of the curly braces in the if statement?
Answer in a comment.
3. Change the values of the variables so that neither message about cats is printed.