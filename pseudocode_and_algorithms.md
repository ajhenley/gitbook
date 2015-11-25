# Pseudocode and Algorithms

###Algorithm
 An algorithm represents the ordered sequence of steps required to solve a problem. Following the steps will always result in the solution. When a computer is to solve a particular problem, the steps to the solution get communicated to the computer. This makes the study of algorithms an important part of computer science.  
 
 The algorithm gets translated to a programming language, such as Java. The Java compiler will translate the program into instructions the computer can execute. This produces the required output from the given input.
 
 But translating the algorithm to computer code is not straight forward.  To simplify the process, next translate the algorithm into pseudocode. The pseudocode will then more easily translate into Java or another programming language.

###Pseudocode
Pseudo code is a human readable representation of an algorithm. It is not written in a specific syntax of any particular programming language. However, a programmer can easily translate pseudocode to Java because the pseudocode is the algorithm plus any considerations for making it into a program.

There is not a standard format for pseudocode. It tends to be a cross between some of the more widely used programming languages and natural language. Pseudocode can generally be read by programmers who are familiar with different programming languages.

Pseudocode allows one to include all the constructs of the Structure Theorem. That means that pseudocode can include sequence, selection and repetition needed to perform the algorithm.

###Pseudocode Conventions
* Statements are written in simple English.
* Each instruction is written on a separate line.
* Keywords and indentation are used to signify particular control structures.
* Each set of instructions is written from top to bottom, with only one entry point and one exit point.
* Groups of statements may be grouped into named modules.


###So what's the difference?
An algorithm is the solution to the problem. It presents a well defined sequence of steps that provides a solution for a given problem. Pseudocode represents the algorithm in a format that resembles any programming language. The client or business analyst derive the algorithm. Someone with knowledge of programming derives the pseudocode. The programmer develops the program from the pseudocode. The compiler translates the program into byte code or machine code and the program runs! The client is happy. And the Project Manager gets all the credit.

###Finally! The example:
####Algorithm:
Our local weatherman tells us how to convert a temperature from Fahrenheit to Celsius. She says to subtract 32 from the Fahrenheit temperature and then multiply that value by 5/9. That's the algorithm.

From that we derive the pseudocode:
<pre>Prompt user for fahreheitTemp 
Get fahreheitTemp
compute celciusTemp = (fahreheitTemp &ndash; 32)* 5/9
Display celciusTemp</pre>

Which one would you rather have in front of you when you're ready to write a program to convert temperatures?
Notice that the pseudocode example has made several decisions for the programmer including the order of operations (note the parenthesis which ensure the calculation is correct), the variable names and the steps to follow. <i>The programmer can now focus on programming and not the business problem</i>. Programmers are often asked to develop solutions for problems they do not fully understand. For the example above, it is unlikely that you are a meteorologist yet you wouldn't need to be because that person already figured out the formula and gave you the algorithm. You just have to program it.
