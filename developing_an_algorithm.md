# Developing an Algorithm

##Defining the Problem

{% em %}
highlighted with a custom color!
{% endem %}

This text is {% em %}highlighted !{% endem %}
 
This text is {% em type="green" %}highlighted in green!{% endem %}
 
This text is {% em type="red" %}highlighted in red!{% endem %}
 
This text is {% em color="#ff0000" %}highlighted with a custom color!{% endem %}


IF THE ALGORITHM IS NOT CORRECT, THE PROGRAM NEVER WILL BE

<p>To help with the initial analysis, the problem should be divided into three separate components:</p>
<p>&nbsp;</p>
<ol>
<li><strong>Input</strong>: a list of the source data provided to the problem.</li>
<li><strong>Output</strong>: a list of the outputs required.</li>
<li><strong>Processing</strong>: a list of the actions needed to produce the required outputs.</li>
</ol>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>When dividing a problem into its three different components, you should simply analyze the actual words used in the specification, and divide them into those that are descriptive and those that imply actions.&nbsp;</p>
<p>&nbsp;In some programming problems, the inputs, processes and outputs may not be clearly defined.&nbsp;</p>
<p>&nbsp;In such cases, it is best to concentrate on the required outputs which will lead to the required inputs needed to produce the desired output.</p>
<p>&nbsp;The nouns and their associated adjectives will determine the inputs and outputs.</p>
<p>&nbsp;The verbs will determine the processing requirements.</p>
<p>&nbsp;</p>
<p>We recommend a three column format as below:</p>
<p>&nbsp;</p>
<table border="1">
<tbody>
<tr>
<td width="197">
<p>Input</p>
</td>
<td width="197">
<p>Processing</p>
</td>
<td width="197">
<p>Output</p>
</td>
</tr>
<tr>
<td width="197">
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
</td>
<td width="197">
<p>&nbsp;</p>
</td>
<td width="197">
<p>&nbsp;</p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<h3>Designing a Solution Algorithm</h3>
<p>Designing a solution algorithm is the most challenging task in the life cycle of a program. &nbsp;Once the problem has been properly defined, you usually begin with a rough sketch of the steps required to solve the problem.&nbsp;The first attempt at designing a particular algorithm usually does not result in a finished product.&nbsp;</p>
<p>Pseudocode is useful in this trial-and-error process, since it is relatively easy to add, delete or alter an instruction.&nbsp;Note that the algorithm starts with a meaningful name and ends with an <strong>END</strong> statement.</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<h3>Checking the Solution Algorithm</h3>
<p>&nbsp;After a solution algorithm has been established, it must be tested for correctness.&nbsp;This step is necessary because most major logic errors occur during the development of the algorithm, and if not detected, these errors can be passed on to the program. &nbsp;Desk checking involves tracing through the logic of the algorithm with some chosen test data.&nbsp;</p>
<p>&nbsp;</p>
<h3>Selecting Test Data</h3>
<p>When selecting test data to desk check an algorithm, you must look at the program specification and choose simple test cases only, <strong>based on the requirements of the specification</strong>, not the algorithm. &nbsp;By doing this, you will still be able to concentrate on <em>what</em> the program is supposed to do, not <em>how.&nbsp;</em></p>
<p>&nbsp;</p>
<h3>Steps in Desk Checking an Algorithm</h3>
<p>By desk checking an algorithm, you are attempting to detect early errors. This process is sometimes called a program walk-through.&nbsp;&nbsp;It is a good idea for someone other than the author of the solution algorithm to design the test data for the program, as they are not influenced by the program logic.&nbsp;Desk checking will eliminate most errors but is not 100% full proof.</p>
<p>&nbsp;</p>
<h3>There are six steps to follow when desk checking an algorithm:</h3>
<ol>
<li>Choose simple input test data cases, two or three</li>
<li>Determine the expected result for each test case before desk checking your algorithm</li>
<li>Make a table of all relevant variables used in the algorithm, variable names at the top of each column</li>
<li>Walk the first test case through the algorithm, line by line, keeping a step-by-step record of the contents of each variable</li>
<li>Repeat the walk-through process for each of the other test cases.</li>
<li>Verify that the expected result from step 2 agrees with the results developed in steps 4 and 5.</li>
</ol>
<p>&nbsp;</p>
<p>If the walk-through results do not agree with the expected results from step 2, revise the algorithm.</p>
<p>&nbsp;</p>