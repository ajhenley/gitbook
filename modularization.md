# Modularization

Modular programming deals with organizing the functionality of a program. After modularization your program becomes a collection of independent, interchangeable components. Each component contains the code necessary to perform its specific functionality. 

When creating programs in Java these modules will become either methods, classes or packages. A method is a unit of code that performs one task. A class generally contains fields and methods which describe the behavior of an object. A package is a collection of related classes. A method in Java will never exist outside of a class.

###What is the interface of a module?
The interface of a method consists of the inputs, outputs, and required processing steps. The interface of a class are those members and methods which are visible to the calling program.

Modular programming refers to the task of decomposing your algorithm into modules. Each module may be reused within the current program or even in other programs. Each method of each module can also be independently tested/verified with unit tests.


<p>Modularization is the process of dividing a problem into separate tasks, each with a single purpose.&nbsp;</p>
<p>Top-down design methodology allows the programmer to concentrate on the overall design of the algorithm without getting too involved with the details of the lower-level modules.&nbsp;&nbsp;&nbsp;</p>
<p>&nbsp;</p>
<h3>The Modularization Process</h3>
<p>When you are defining the problem, write down the tasks or processing steps which would solve your problem. A module must be large enough to perform its single task, and must include only the operations that contribute to the performance of that task.&nbsp;It should have a single entry, and a single exit with a top-to-bottom sequence of instructions. &nbsp;The name of the module should describe the work to be done as a single specific function.&nbsp; Name each module by using a verb, followed by a one or two-word object.&nbsp;One module can call or evoke another module.&nbsp; This passes control the called module.&nbsp; When the called module terminates control is passed back to the calling module.</p>
<p>&nbsp;</p>
<h3>The Main Routine - your starting point</h3>
<p>The main routine is the starting point for your program. The main routine ties all the modules together and coordinates their activity. The main routine contains the main processing functions, and the order in which they will execute. It also shows the flow of data and the major control structures. The main program should be easy to read, be of manageable length and show the logic structure of the program.</p>

The signature of the main routine in a Java program is:<br/>
    public static void main(String args[])


<h3>Benefits of Modular Design</h3>
<ul>
<li>Ease of understanding &ndash; each module performs only one function</li>
<li>Reusable code &ndash; the single function can be used by multiple other modules</li>
<li>Elimination of redundancy &ndash; no need to repeat writing the same code</li>
<li>Efficiency of maintenance &ndash; changes to the logic of one module will have little or no effect on other modules</li>
<li>Ease of testing &ndash; unit tests can confirm the functionality of each method in your module.
</ul>
<p>&nbsp;</p>