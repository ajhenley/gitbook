# Pseudocode and Algorithms

<h3>Algorithm</h3>
<p>An algorithm is a procedure for solving a problem in terms of the actions to be executed and the order in which those actions are to be executed. An algorithm is merely the sequence of steps taken to solve a problem.&nbsp;An algorithm gives a solution to a particular problem as a well defined set of steps. A recipe in a cookbook is a good example of an algorithm.</p>
<p>When a computer is used for solving a particular problem, the steps to the solution should be communicated to the computer. This makes the study of algorithms a very important part of&nbsp;computer science. An algorithm is executed in a computer by combining lot of elementary operations such as addition and subtraction to perform more complex mathematical operations.</p>
<p>But translating the idea of the algorithm to computer code is not straight forward so you take the next step and translate the algorithm into pseudocode. The pseudocode will then more easily translate into Java or any other programming language.</p>
<h3>Pseudocode</h3>
<p><span>Pseudo code is a human readable representation of an algorithm.&nbsp;</span>It is not written in a specific syntax that is used by a programming language and so it can't&nbsp;be executed on a computer. However, a programmer can more easily translate pseudocode to Java because the pseudocode is the algorithm plus any considerations for making it into a program.&nbsp;</p>
<p>There is not a standard format for pseudocode but it tends to be a cross between some of the more widely used programming languages and natural language. Pseudocode can generally be read by programmers who are familiar with different programming languages.</p>
<p>Pseudocode allows one to include control structures such as IF-THEN-ELSE, DOWHILE, REPEAT-UNTIL which are present in many high level languages.</p>
<p><strong><span style="text-decoration: underline;">Pseudocode Conventions</span></strong></p>
<ul>
<li>Statements are written in simple English.</li>
<li>Each instruction is written on a separate line.</li>
<li>Keywords and indentation are used to signify particular control&nbsp;structures.</li>
<li>Each set of instructions is written from top to bottom, with only one entry&nbsp;and one exit.</li>
<li>Groups of statements may be formed into modules, and that module given&nbsp;a name.</li>
</ul>
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