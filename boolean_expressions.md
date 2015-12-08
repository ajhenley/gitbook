# Boolean expressions

Boolean Expressions
So far we have only seen three types of variables:

int
integers, hold numbers (positive or negative) with no fractional parts
double
“double-precision floating-point” numbers (positive or negative) that could have a fractional part
String
a string a characters, hold words, phrases, symbols, sentences, whatever
But in the words of Yoda: “There is another.” A “Boolean” variable (named after the mathematician George Boole) cannot hold numbers or words. It can only store one of two values: true or false. That’s it. We can use them to perform logic. To the code!
```
 1 import java.util.Scanner;
 2 
 3 public class BooleanExpressions
 4 {
 5     public static void main( String[] args )
 6     {
 7         Scanner keyboard = new Scanner(System.in);
 8 
 9         boolean a, b, c, d, e, f;
10         double x, y;
11 
12         System.out.print( "Give me two numbers. First: " );
13         x = keyboard.nextDouble();
14         System.out.print( "Second: " );
15         y = keyboard.nextDouble();
16 
17         a = (x <  y);
18         b = (x <= y);
19         c = (x == y);
20         d = (x != y);
21         e = (x >  y);
22         f = (x >= y);
23 
24         System.out.println( x + " is LESS THAN " + y + ": " + a );
25         System.out.println( x + " is LESS THAN or EQUAL TO " + y + ": " + b );
26         System.out.println( x + " is EQUAL TO " + y + ": " + c );
27         System.out.println( x + " is NOT EQUAL TO " + y + ": " + d );
28         System.out.println( x + " is GREATER THAN " + y + ": " + e );
29         System.out.println( x + " is GREATER THAN or EQUAL TO " + y + ": " + f );
30         System.out.println();
31 
32         System.out.println( !(x < y) + " " + (x >= y) );
33         System.out.println( !(x <= y) + " " + (x > y) );
34         System.out.println( !(x == y) + " " + (x != y) );
35         System.out.println( !(x != y) + " " + (x == y) );
36         System.out.println( !(x > y) + " " + (x <= y) );
37         System.out.println( !(x >= y) + " " + (x < y) );
38 
39     }
40 }```
What You Should See
Give me two numbers. First: 3
Second: 4
3.0 is LESS THAN 4.0: true
3.0 is LESS THAN or EQUAL TO 4.0: true
3.0 is EQUAL TO 4.0: false
3.0 is NOT EQUAL TO 4.0: true
3.0 is GREATER THAN 4.0: false
3.0 is GREATER THAN or EQUAL TO 4.0: false

false false
false false
true true
false false
true true
true true

On line 17 the Boolean variable a is set equal to something strange: the result of a comparison. The current value in the variable x is compared to the value of the variable y. If x is less than y, then the comparison is true and the Boolean value true is stored into a. If x is not less than y, then the comparison is false and the boolean value false is stored into a. (I think that is easier to understand than it is to write.)

Line 18 is similar, except that the comparison is “less than or equal to”, and the Boolean result is stored into b.

Line 19 is “equal to”: c will be set to the value true if x holds the same value as y. The comparison in line 20 is “not equal to”. Lines 21 and 22 are “greater than” and “greater than or equal to”, respectively.

On lines 24 through 29, we display the values of all those Boolean variables on the screen.

Line 32 through line 37 introduce the “not” operator, which is an exclamation point (!). It takes the logical opposite. So on line 32 we display the logical negation of “x is less than y?”, and we also print out the truth value of “x is greater than or equal to y?”, which are equivalent. (The opposite of “less than” is “greater than or equal to”.) Lines 33 through 37 show the opposites of the remaining relational operators.