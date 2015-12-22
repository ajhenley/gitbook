# Selection Control Structures

<p><strong>The Selection Control Structure</strong></p>
<p>&nbsp;You can use the selection control structure in pseudocode to illustrate a choice between two or more actions, depending on whether a condition is true or false.&nbsp;</p>
<p>&nbsp;</p>
<p><span style="text-decoration: underline;">General Format:</span></p>
<p>&nbsp;<strong>IF</strong> [condition]</p>
<p><strong>THEN</strong></p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [true actions]</p>
<p><strong>ELSE</strong></p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [false actions]</p>
<p><strong>ENDIF</strong></p>
<p>&nbsp;</p>
<p>The condition in the <strong>IF </strong>statement is based on a comparison of two items, and is usually expressed with one of the following relational operators:</p>
<p>&nbsp;</p>
<p>&lt;&nbsp;&nbsp; less than &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; greater than</p>
<p>=&nbsp;&nbsp; equal to&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &lt;=&nbsp;&nbsp;&nbsp;&nbsp; less than or equal to</p>
<p>&gt;= greater than or equal to&nbsp; &lt; &gt;&nbsp;&nbsp;&nbsp; not equal to</p>
<p>&nbsp;</p>
<p>When the condition following the <strong>IF</strong> is true only the actions following the <strong>THEN</strong> and before the <strong>ELSE</strong> are performed.</p>
<p>When the condition following the <strong>IF</strong> is false only the actions following the <strong>ELSE</strong> and before the <strong>ENDIF</strong> are performed.</p>
<p>&nbsp;</p>
<p>There are a number of variations of the <strong>IF</strong> statement.</p>
<p>&nbsp;</p>
<p><strong><br /> </strong></p>
<h3>Simple Selection (simple IF statement)</h3>
<p>&nbsp;</p>
<p>Simple selection occurs when a choice is made between two alternate paths, depending on the result of a condition being true or false.&nbsp;</p>
<p>&nbsp;The structure is represented in pseudocode using the keywords <strong>IF, THEN, ELSE </strong>and<strong> ENDIF</strong>.&nbsp;</p>
<p>&nbsp;</p>
<p><span style="text-decoration: underline;">Example:</span></p>
<p>&nbsp;<strong>IF</strong> Gender = &ldquo;M&rdquo;</p>
<p><strong>THEN</strong></p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Add 1 to Male-Count</p>
<p><strong>ELSE</strong></p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Add 1 to Female-Count</p>
<p><strong>ENDIF</strong></p>
<p>&nbsp;</p>
<h3>Simple Selection with Null False Branch (null ELSE statement)</h3>
<p>&nbsp;It is used when a task is performed only when a particular condition is true.&nbsp;</p>
<p>&nbsp;If the condition is false, then no processing will take place and the <strong>IF</strong> statement will be bypassed.&nbsp;&nbsp;&nbsp;</p>
<p>&nbsp;</p>
<p>The <strong>ELSE</strong> clause is not used.&nbsp;</p>
<p>&nbsp;</p>
<p><span style="text-decoration: underline;">Example:</span></p>
<p>&nbsp;<strong>IF</strong> Age &gt; 18</p>
<p><strong>THEN</strong></p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Add 1 to Adult-Count</p>
<p><strong>ENDIF</strong></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<h3>Combined Selection (combined IF statement)</h3>
<p>&nbsp;</p>
<p>A combined IF statement is one that contains multiple conditions, each connected with the logical operators <strong>AND</strong> or <strong>OR</strong>.&nbsp;</p>
<p>If the connector <strong>AND</strong> is used to combine two conditions, then <strong><u>both</u></strong> conditions must be true for the combined condition to be true.&nbsp;</p>
<p>If the connector <strong>OR</strong> is used to combine two conditions, then <strong><u>only one</u></strong> of the conditions needs to be true for the combined condition to be considered true.</p>
<p>&nbsp;</p>
<p><span style="text-decoration: underline;">Examples:</span></p>

```
IF Gender = "M" THEN
    Add 1 to Male-Count
ELSE
    Add 1 to Female-Count
ENDIF
```
<h3>The NOT operator</h3>
<p>The <strong>NOT</strong> operator can be used for the logical negation of a condition as follows:</p>
<p>&nbsp;<strong>IF NOT</strong> (Record-Code = &rsquo;23&rsquo;)</p>
<p><strong>THEN </strong></p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Update customer record</p>
<p><strong>ENDIF </strong></p>
<p>&nbsp;</p>
<h3>Nested Selection (nested IF statement)</h3>
<p>&nbsp;A nested selection occurs when the word <strong>IF</strong> appears more than once within an <strong>IF</strong> statement.&nbsp;</p>
<p>&nbsp;A nested <strong>IF</strong> statements can be classified as linear or non-linear.&nbsp;</p>
<p>&nbsp;</p>
<h3>Linear nested IF statements</h3>
<p>The linear nested <strong>IF</strong> statement is used when a field is being tested for various values and a different action is to be taken for each value.&nbsp;</p>
<p>This form of nested <strong>IF</strong> is called linear, because each <strong>ELSE</strong> immediately follows the <strong>IF</strong> condition to which it corresponds.&nbsp;</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</p>
<table border="1" width="559">
<tbody>
<tr>
<td width="103">
<p>Example:</p>
</td>
<td width="168">
<p><strong>Transaction Code</strong></p>
</td>
<td width="288">
<p><strong>Action</strong></p>
</td>
</tr>
<tr>
<td width="103">
<p>&nbsp;</p>
</td>
<td width="168">
<p>A</p>
</td>
<td width="288">
<p>Add a new customer record</p>
</td>
</tr>
<tr>
<td width="103">
<p>&nbsp;</p>
</td>
<td width="168">
<p>C</p>
</td>
<td width="288">
<p>Change customer record</p>
</td>
</tr>
<tr>
<td width="103">
<p>&nbsp;</p>
</td>
<td width="168">
<p>D</p>
</td>
<td width="288">
<p>Delete customer record</p>
</td>
</tr>
<tr>
<td width="103">
<p>&nbsp;</p>
</td>
<td width="168">
<p>Any other code</p>
</td>
<td width="288">
<p>Display error message</p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<p><strong>IF</strong> Tran-Code = &ldquo;A&rdquo;</p>
<p><strong>THEN</strong></p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Add a new customer record</p>
<p><strong>ELSE</strong></p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>IF</strong> Tran-Code = &ldquo;C&rdquo;</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>THEN</strong></p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Change customer record</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>ELSE</strong></p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>IF</strong> Tran-Code = &ldquo;D&rdquo;</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>THEN</strong></p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Delete customer record</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>ELSE</strong></p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Display error message</p>
<p><strong>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ENDIF</strong></p>
<p><strong>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ENDIF</strong></p>
<p><strong>ENDIF</strong></p>
<p><strong><br /> </strong></p>
<h3>Nested Selection (nested IF statement) &ndash; continued</h3>
<p>&nbsp;A non-linear nested <strong>IF</strong> occurs when a number of different conditions need to be satisfied before a particular action can occur.&nbsp;&nbsp;It is termed non-linear because the <strong>ELSE</strong> statement may be separated from the <strong>IF</strong> statement with which it is paired.&nbsp;</p>
<p>&nbsp;</p>
<table border="1" width="583">
<tbody>
<tr>
<td width="99">
<p>Example:</p>
</td>
<td width="128">
<p><strong>Condition 1</strong></p>
</td>
<td width="126">
<p><strong>Condition 2</strong></p>
</td>
<td width="231">
<p><strong>Action</strong></p>
</td>
</tr>
<tr>
<td width="99">
<p>&nbsp;</p>
</td>
<td width="128">
<p>Salaried Employee</p>
</td>
<td width="126">
<p>&nbsp;</p>
</td>
<td width="231">
<p>Pay base salary</p>
</td>
</tr>
<tr>
<td width="99">
<p>&nbsp;</p>
</td>
<td width="128">
<p>Hourly Employee</p>
</td>
<td width="126">
<p>Hours &lt;= 40</p>
</td>
<td width="231">
<p>Calculate pay at hourly rate</p>
</td>
</tr>
<tr>
<td width="99">
<p>&nbsp;</p>
</td>
<td width="128">
<p>Hourly Employee</p>
</td>
<td width="126">
<p>Hours &gt; 40</p>
</td>
<td width="231">
<p>Calculate pay with overtime</p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<p><strong>IF</strong> Employee-Code = &ldquo;H&rdquo;</p>
<p><strong>THEN</strong></p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>IF</strong> Hours-Worked &lt;= 40</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>THEN</strong></p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Calculate pay at hourly rate</p>
<p><strong>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ELSE</strong></p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Calculate pay with overtime</p>
<p><strong>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ENDIF</strong></p>
<p><strong>ELSE</strong></p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Pay base salary</p>
<p><strong>ENDIF</strong></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<h3><strong>The Case Structure</strong></h3>
<p>&nbsp;The <strong>CASE</strong> control structure in pseudocode is another way of expressing a linear nested <strong>IF</strong> statement.&nbsp;</p>
<p>It is used in pseudocode for two reasons:</p>
<ol>
<li>It can be directly translated into many high-level languages, and</li>
<li>It makes the pseudocode easier to write and understand.&nbsp;</li>
</ol>
<p>Using nested IF statements in pseudocode often look cumbersome and depend on correct structure and indentation for readability.&nbsp;</p>
<p>&nbsp;</p>
<h3>General format:</h3>
<p><strong>CASE OF</strong> variable-name</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>VALUE-1:</strong> statement block-1</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>VALUE-2:</strong> statement block-2</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>VALUE-3:</strong> statement block-3</p>
<p><strong>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .</strong></p>
<p><strong>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .</strong></p>
<p><strong>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .</strong></p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>VALUE-n:</strong> statement block-n</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>VALUE-OTHER:</strong> statement block-other</p>
<p><strong>ENDCASE</strong></p>
<p>&nbsp;</p>
<p>The value of the &ldquo;variable-name&rdquo; is compared to each VALUE-n from the top down.&nbsp;When there is an equal condition the corresponding &ldquo;statement block&rdquo; is executed.&nbsp;If there is no match the VALUE-OTHER &ldquo;statement block&rdquo; is executed.</p>
<p>&nbsp;</p>
<p>Example:</p>
<table border="1" width="559">
<tbody>
<tr>
<td width="99"></td>
<td width="128">
<p><strong>Condition </strong></p>
</td>
<td width="333">
<p><strong>Action</strong></p>
</td>
</tr>
<tr>
<td width="99">
<p>&nbsp;</p>
</td>
<td width="128">
<p>Age &lt; &nbsp;&nbsp;3</p>
</td>
<td width="333">
<p>Ticket Price =&nbsp;&nbsp; 25% of standard fare</p>
</td>
</tr>
<tr>
<td width="99">
<p>&nbsp;</p>
</td>
<td width="128">
<p>Age &lt; 13</p>
</td>
<td width="333">
<p>Ticket Price =&nbsp;&nbsp; 50% of standard fare</p>
</td>
</tr>
<tr>
<td width="99">
<p>&nbsp;</p>
</td>
<td width="128">
<p>Age &lt; 20</p>
</td>
<td width="333">
<p>Ticket Price = 150% of standard fare</p>
</td>
</tr>
<tr>
<td width="99">
<p>&nbsp;</p>
</td>
<td width="128">
<p>Age &gt; 64</p>
</td>
<td width="333">
<p>Ticket Price =&nbsp;&nbsp; 50% of standard fare</p>
</td>
</tr>
<tr>
<td width="99">
<p>&nbsp;</p>
</td>
<td width="128">
<p>Other</p>
</td>
<td width="333">
<p>Ticket Price = 100% of standard fare</p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<p><strong>&nbsp;</strong></p>
<p><strong>CASE OF</strong> age</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>&lt;&nbsp;&nbsp; 3:</strong> Calculate Ticket Price = &nbsp;&nbsp;25% of standard fare</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>&lt; 13:</strong> Calculate Ticket Price =&nbsp; &nbsp;50% of standard fare</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>&lt; 20:</strong> Calculate Ticket Price = 150% of standard fare</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>&gt; 64:</strong> Calculate Ticket Price =&nbsp;&nbsp; 50% of standard fare</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>VALUE_OTHER:</strong> Calculate Ticket Price = 100% of standard fare</p>
<p><strong>ENDCASE</strong></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>