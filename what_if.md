###If
Here is the next Java program you'll enter, which introduces you to the if statement. Type this in, make it run exactly right and then we'll see if your practice has paid off.

The if statement helps us make decisions and control program flow. In the program below, only one line prints but there are 7 ```System.out.print``` statements. The ```if``` statement ensures that only the correct one is executed.

####Hurricane wind speed chart
|Category|Wind Speed (mph)|
|-|-|
|1|74 - 95|
|2|96 - 110|
|3|111 - 130|
|4|131 - 155|
|5|155 and above|


```java
public class Hurricane {

	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);
		System.out.print("How fast was the wind blowing?" );
		int windSpeed = scan.nextInt();

        if (windSpeed <  65) 
        	System.out.println("It was not a hurricane");
        else if (windSpeed <  96) 
        	System.out.println("It was a class 1 hurricane");      
        else if (windSpeed < 111) 
        	System.out.println("It was a class 2 hurricane");      
        else if (windSpeed < 131) 
        	System.out.println("It was a class 3 hurricane");      
        else if (windSpeed < 155) 
        	System.out.println("It was a class 4 hurricane");      
        else
        	System.out.println("It was a class 5 hurricane");
 
	}
}
```

####Your assignment
Write a program to accept an integer from the user. The program should print the integer or  'Fizz','Buzz' or 'FizzBuzz' as indicated by the rules below:
    For numbers 1 through 100,
    if the number is divisible by 3 print Fizz;
    if the number is divisible by 5 print Buzz;
    if the number is divisible by 3 and 5 (15) print FizzBuzz;
    else, print the number.

