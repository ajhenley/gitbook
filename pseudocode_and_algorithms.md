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


<h3>So what's the difference?</h3>
<p>An algorithm is the solution to the problem. It presents a well defined sequence of steps that provides a solution for a given problem. Pseudocode is a method that represents the algorithm in a format that resembles a programming language.</p>
<p>Pseudocode does not use specific programming language syntax so it is&nbsp;understood by programmers who are familiar with different programming languages. Additionally, transforming an algorithm presented in pseudocode to programming code could be much easier than converting an algorithm written in natural language.</p>
<p>&nbsp;</p>
<h3>Finally!&nbsp;The example:</h3>
<h4>Algorithm:</h4>
<p>To convert a temperature from Fahrenheit to Celsius you would subtract 32 from the Fahrenheit temperature and then multiply that value by 5/9.</p>
<h4>Pseudocode:&nbsp;</h4>
<p>Prompt operator for f_temp<br />Get f_temp<br />compute c_temp = (f_temp &ndash; 32)* 5/9<br />Display c_temp</p>
<p><em>Which one would you rather have in front of you when you're ready to write a program to convert temperatures?</em></p>
<p><em>Notice that the pseudocode example has made several decisions for the programmer including the order of operations (note the parenthesis which ensure the calculation is correct), the variable names and the steps to follow. The programmer can now spend time focusing on programming and not thinking about the business problem. Many times as programmers you will be asked&nbsp;to develop solutions for problems you do not fully understand. For the example above, it is unlikely that you are a&nbsp;meteorologist&nbsp;yet you wouldn't need to be because that person&nbsp;already figured&nbsp;out the formula and gave you the algorithm. You just have to program it.</em></p>
<p>&nbsp;</p>
<p>&nbsp;</p>