# Modularization

Modular programming is a software design technique that emphasizes separating the functionality of a program into independent, interchangeable modules, such that each contains everything necessary to execute only one aspect of the desired functionality.

###What is the interface of a module?
Inputs, outputs and processing steps


<p>Modularization is the process of dividing a problem into separate tasks, each with a single purpose.&nbsp;</p>
<p>Top-down design methodology allows the programmer to concentrate on the overall design of the algorithm without getting too involved with the details of the lower-level modules.&nbsp;&nbsp;&nbsp;</p>
<p>&nbsp;</p>
<h3>The Modularization Process</h3>
<p>When you are defining the problem, write down the activities or processing steps to be performed.&nbsp;A module must be large enough to perform its single task, and must include only the operations that contribute to the performance of that task.&nbsp;It should have a single entry, and a single exit with a top-to-bottom sequence of instructions. &nbsp;The name of the module should describe the work to be done as a single specific function.&nbsp; Name each module by using a verb, followed by a one or two-word object.&nbsp;One module can call or evoke another module.&nbsp; This passes control the called module.&nbsp; When the called module terminates control is passed back to the calling module.</p>
<p>&nbsp;</p>
<h3>The Mainline</h3>
<p>A mainline routine must provide the master control that ties all the modules together and coordinates their activity. &nbsp;This program mainline should show the main processing functions, and the order in which they are to be performed.&nbsp;It should also show the flow of data and the major control structures. &nbsp;The mainline should be easy to read, be of manageable length and show the logic structure of the program.</p>
<h6>&nbsp;</h6>
<h3>Benefits of Modular Design</h3>
<ul>
<li>Ease of understanding &ndash; each module performs only one function</li>
<li>Reusable code &ndash; the single function can be used by multiple other modules</li>
<li>Elimination of redundancy &ndash; no need to repeat writing the same code</li>
<li>Efficiency of maintenance &ndash; changes to the logic of one module will have little or no effect on other modules</li>
</ul>
<p>&nbsp;</p>