# Coding arithmetic statements
<!--test comment--->
####Mathematical Operations
Now that we know how to declare and initialize variables in Java, we can do some mathematics with those variables.

```java
 1 public class MathOperations
 2 {
 3     public static void main( String[] args )
 4     {
 5         int a, b, c, d, e, f, g;
 6         double x, y, z;
 7         String one, two, both;
 8 
 9         a = 10;
10         b = 27;
11         System.out.println( "a is " + a + ", b is " + b );
12 
13         c = a + b;
14         System.out.println( "a+b is " + c );
15         d = a - b;
16         System.out.println( "a-b is " + d );
17         e = a+b*3;
18         System.out.println( "a+b*3 is " + e );
19         f = b / 2;
20         System.out.println( "b/2 is " + f );
21         g = b % 10;
22         System.out.println( "b%10 is " + g );
23 
24         x = 1.1;
25         System.out.println( "\nx is " + x );
26         y = x*x;
27         System.out.println( "x*x is " + y );
28         z = b / 2;
29         System.out.println( "b/2 is " + z );
30         System.out.println();
31 
32         one = "dog";
33         two = "house";
34         both = one + two;
35         System.out.println( both );
36     }
37 }
```

<h1>What You Should See</h1>
<pre>
a is 10, b is 27
a+b is 37
a-b is -17
a+b*3 is 91
b/2 is 13
b%10 is 7

x is 1.1
x*x is 1.2100000000000002
b/2 is 13.0

doghouse

</pre>

The plus sign (+) will add two integers or two doubles together, or one integer and one double (in either order). With two Strings (like on line 34) it will concatenate the two Strings together.

The minus sign (-) will subtract one number from another. Just like addition, it works with two integers, two doubles, or one integer and one double (in either order).

An asterisk (*) is used to represent multiplication. You can also see on line 17 that Java knows about the correct order of operations. <em>b</em> is multiplied by 3 giving 81 and then <em>a</em> is added.

A slash (/) is used for division. Notice that when an integer is divided by another integer (like on line 19) the result is also an integer and not a double.

The percent sign (%) is used to mean &lsquo;modulus&rsquo;, which is essentially the remainder left over after dividing. On line 21, <em>b</em> is divided by 10 and the remainder (7) is stored into the variable <em>g</em>.

####Common Student Questions
* Why is 1.1 times 1.1 equal to 1.2100000000000002 instead of just 1.21?
<blockquote>
Why is 0.333333 + 0.666666 equal to 0.999999 instead of 1.0? Sometimes with math we get repeating decimals, and most computers convert numbers into binary before working with them. It turns out that 1.1 is a repeating decimal in binary. <p>
Remember what I said in the last exercise: the problem with doubles is limited precision. You will mostly be able to ignore that fact in this book, but I would like you to keep in the back of your mind that double variables sometimes give you values that are <em>slightly</em> different than you&rsquo;d expect.
</blockquote>
