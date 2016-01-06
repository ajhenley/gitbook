###Creating new data types in Java
So far we've seen eight primitive data types. These have determined the type of data our programs can store and work with. We can work with integers, floating point numbers, Boolean values, Strings and others. 

What if you have data you want to store that is more complex than numbers or letters? What if you want to work with a Date? You want to be able to add days to the date, to get the number of days between two dates and to find the last day in a particular month. And you want other programmers to be able to do the same. But you want the data type to figure all that out for you.

Lucky for us Java enables us create our own Date data type. How? By creating a class. We can include fields for month, day and year. We can even include a method to display our date.

Our class would look like this:
{%ace edit=true, lang='java'%}
public class DateProcessor {
	public int month = 1;
	public int day = 1;
	public int year = 1970;
	
	public String displayDate(){
		return month + "-" + day + "-" + year;
				
	}
}
{%endace%}

And work like this:
{%ace edit=true, lang='java'%}
public class StartHere {
	public static void main(String[] args){
		DateProcessor dp = new DateProcessor();
		dp.month = 5;
		dp.day = 23;
		dp.year = 1995;
		
		System.out.printf("Java was born on %s\n", dp.displayDate());
				
	}

}
{%endace%}

This is fabulous! Our own data type. All our problems are solved. I can set the month, day and year and return the date. Programmers all over can use our date type to save time displaying dates. What could go wrong?

What happen if the programmer tries to enter 360 for the month? And what about 2/31/2015? Can we fix that?

Our own data type will allow us to guarantee that a date is actually a valid date. We’ll just include more methods to ensure that the values are valid. 

Let’s start with getting and setting the month, day and year.


