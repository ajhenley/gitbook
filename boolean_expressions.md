###Boolean expressions

A boolean variable can hold one of two values: true or false. A boolean expression is an expression that can return one of two values: true or false. 

Boolean expressions are most often used in if statements. You test the value of an expression and use that value to determine where your program goes.

####Legal boolean expressions
In an if statement the legal expression is a boolean. Some programming languages allow you to use 1 for true or 0 for false. Not Java. Java requires an expression which evaluates to true or false. ```if (1)``` is not legal but ```if (1==1)``` is legal.

####An example
```java
if (x > 3) {
    System.out.println("x is greater than 3");
}else{
    System.out.println("x is less than or equal to 3");
}
```

