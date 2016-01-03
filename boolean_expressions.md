<!--djw:done-->
<!--ajh:done-->

###Boolean decisions

A boolean variable can hold one of two values: true or false. A boolean expression is an expression that can return one of two values: true or false. 

Boolean expressions are often used when making decisions. This means you'll want to be comfortable using boolean expressions in if-statements. To do this, you test the value of an expression. You can use that value to determine where your program goes.

####Example:
{%ace edit=false, lang='java'%}
System.out.print("Enter your test score: ");
		int score = scan.nextInt();
		char grade = 'F';//I'm not hopeful

		if (score > 89)
		    grade = 'A';
		else if (score > 79)
		    grade = 'B';
		else if (score > 69)
		    grade = 'C';
		else 
		    grade = 'F';

		if (score > 69)
		    System.out.println("Very good! You don't have to retake the exam!");
		else
		    System.out.println("Did you even look at the book?");
    
{%endace%}

####Saying No!
You can negate a boolean expression with the ```!``` operator.

####Legal boolean expressions
In an if-statement the legal expression is a boolean. Some programming languages allow you to use 1 for true or 0 for false. Not Java. Java requires an expression which evaluates to true or false. ```if (1)``` is not legal but ```if (1==1)``` is legal.

####An example
{%ace edit=false, lang='java'%}
if (x > 3) {
    System.out.println("x is greater than 3");
}else{
    System.out.println("x is less than or equal to 3");
}
{%endace%}

####Assignment
Enter the grades example above. Modify the program so a student could get a 'D' if they score between 61 and 70. Also, modify the program to print a + or -   after the letter grade based on the last digit of the score. If the last digit is between 1 and 3 then print a - after the grade. If the last digit is 8,9 or 0 then print a + after the grade. Otherwise don't print a + or - if the last digit is between 4 and 7. Change the output to print the student's grade.

Write a program that allows the user to enter the length of the three sides of a triangle. The program should then display  whether the triangle is an equilateral triangle or not. If the triangle is not an equilateral triangle then the program should display if the triangle is a right triangle or not. The Pythagorean theorem tells us that the square of one side equals the sum of the squares of the other sides for all right triangles.

