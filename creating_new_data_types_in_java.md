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

What if ... a programmer tries to enter 360 for the month? And tries to set the date to 2/31/2015? Can we fix that?

####Improving our class
Our own data type will allow us to guarantee that a date is actually a valid date. We’ll just include more methods to ensure that the values are valid. While we're at it let's include methods to return the number of days in the month. And whether the year is a leap year.

The first thing we do is prevent the programmer from changing the month day and year to crazy values. We start by setting those member variables to private. Then limit access to them by creating methods called getters and setters. These methods can validate the incoming values. Or set defaults.

After a little rework this is our new, even-more-fabulous than the last fabulous DateProcessor.
{%ace edit=true, lang='java'%}
public class DateProcessor {

	private int month = 1;
	private int day = 1;
	private int year = 1970;
	
	public int getMonth() {
		return month;
	}

	public void setMonth(int month) {
		if (month >0 && month<=12){
		    this.month = month;
		}
	}

	public int getNumberDaysInMonth() {
		int lastDay = 31;
		
		switch (month){
		case 1:
		case 3:
		case 5:
		case 7:
		case 8:
		case 10:
		case 12:
			lastDay = 31;
			break;
		case 11:
		case 4:
		case 9:
		case 6:	
			lastDay = 30;
			break;
		case 2:	
			if (isLeapYear()){
				lastDay = 29;
			}else{
				lastDay = 28;
			}
			break;
		}
		
		return lastDay;
	}
	public boolean isLeapYear(){
        // is it divisible by 4?
        boolean bLeapYear = false;
        bLeapYear = (year % 4 == 0);

        // is it divisible by 4 and not 100
        bLeapYear = bLeapYear && (year % 100 != 0);

        // is it divisible by 4 and not 100 unless it's divisible by 400
        bLeapYear = bLeapYear || (year % 400 == 0);
        
        return bLeapYear;
	}

	public void setDay(int day) {
		if (day <= getNumberDaysInMonth() && day >=1){
		    this.day = day;
		}else{
			day = 1;
		}
	}

	public int getYear() {
		return year;
	}

	public void setYear(int year) {
		if (year > 1 && year <=4000){
			this.year = year;
		}else{
			this.year = 1970;
		}
	}


	
	public String displayDate(){
		return month + "-" + day + "-" + year;
				
	}
	
}
{%endace%}


###Your assignment
Now that you've seen how it's done, create a class that has private member variables for first name, last name and age. Then create getters and setters for each. Next, use your new class in the main routine setting the three variables and printing the following:
```System.out.printf("My full name is %s and I am %d years old.",MyClass.fullName,MyClass.age);```


