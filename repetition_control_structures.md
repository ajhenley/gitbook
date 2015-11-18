# Repetition Control Structures

<p>There are three different ways that a set of instructions can be repeated, and each way is determined by where the decision to repeat is placed:&nbsp;</p>
<ul>
<li>at the beginning of the loop (leading decision loop)</li>
<li>at the end of the loop (trailing decision loop)</li>
<li>a counted number of times (counted loop)</li>
</ul>
<p><strong>&nbsp;</strong></p>
<p><strong>Repetition Using the DOWHILE Structure </strong></p>
<p>The <strong>DOWHILE</strong> construct is a <em>leading decision loop</em> &ndash; that is, the condition is tested <strong><u>before</u></strong> any statements are executed.&nbsp;</p>
<p>&nbsp;General format:</p>
<p><strong>DOWHILE </strong>condition p is true&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </strong></p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Statement block&nbsp; <strong>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </strong></p>
<p><strong>ENDDO&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </strong></p>
<p>&nbsp;</p>
<p>There are two important considerations about which you must be aware before designing a <strong>DOWHILE </strong>loop.</p>
<ol>
<li>The testing of the condition is at the beginning of the loop.</li>
<li>The only way to terminate the loop is to render the <strong>DOWHILE </strong>condition false.&nbsp;</li>
</ol>
<p>&nbsp;</p>
<h3>Using DOWHILE to Repeat a Set of Instructions a Known Number of Times</h3>
<p>When a set of instructions is repeated a specific number of times, a counter can be used in pseudocode.</p>
<p>For this construct two actions must be indicated:</p>
<ol>
<li>The counter is initialized before the <strong>DOWHILE</strong> statement and</li>
<li>The counter is incremented before the <strong>ENDDO</strong> statement.&nbsp;</li>
</ol>
<p>&nbsp;</p>
<h3>Using DOWHILE to Repeat a Set of Instructions an Unknown Number of Times</h3>
<p>Often, a trailer record or sentinel signifies the end of the data.&nbsp;</p>
<p>This sentinel is a special record or value placed at the end of valid data to signify the end of that data.&nbsp;</p>
<p>It must contain a value that is clearly distinguishable from the other data to be processed.&nbsp;</p>
<p>&nbsp;</p>
<h3>When a trailer record does not exist &ndash; the most common approach</h3>
<p>When there is no trailer record to signify the end of the data, the programmer needs to check for an end-of-file marker (EOF).&nbsp;</p>
<p>This EOF marker is added when the file is created, as the last character in the file.&nbsp;</p>
<p>The check for EOF is positioned in the <strong>DOWHILE</strong> clause, using one of the following equivalent expressions:</p>
<p><strong>DOWHILE</strong> more data&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</p>
<p><strong>DOWHILE</strong> more records</p>
<p><strong>DOWHILE</strong> records exist&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</p>
<p><strong>DOWHILE </strong><strong>NOT EOF</strong></p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<h3>Repetition Using the REPEAT&hellip;UNTIL Structure</h3>
<p>The <strong>REPEAT&hellip;UNTIL</strong> structure is similar to the <strong>DOWHILE&hellip;ENDDO</strong> structure, in that a group of statements are repeated in accordance with a specified condition.&nbsp;</p>
<p>However, where the <strong>DOWHILE&hellip;ENDDO</strong> structure tests the condition at the beginning of the loop; a <strong>REPEAT&hellip;UNTIL</strong> structure tests the condition at the end of the loop.&nbsp;</p>
<p>The <strong>REPEAT&hellip;UNTIL</strong> is a <em>trailing decision loop</em>; the statements are executed once before the condition is tested.&nbsp;</p>
<p>&nbsp;</p>
<p>There are two other considerations about which you need to be aware before using <strong>REPEAT&hellip;UNTIL</strong>.&nbsp;</p>
<ol>
<li><strong>REPEAT&hellip;UNTIL</strong> loops are executed when the condition is false; it is only when the condition becomes true that repetition ceases.</li>
<li>The statements within a <strong>REPEAT&hellip;UNTIL</strong> structure will always be executed at least once.&nbsp;</li>
</ol>
<p>&nbsp;</p>
<h4>&nbsp;General formats:</h4>
<p>&nbsp;</p>
<table width="583">
<tbody>
<tr>
<td width="247">
<p><strong>REPEAT</strong></p>
</td>
<td width="60">
<p>&nbsp;</p>
</td>
<td width="276">
<p><strong>DOUNTIL</strong> condition p is true</p>
</td>
</tr>
<tr>
<td width="247">
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Statement block</p>
</td>
<td width="60">
<p><strong>OR</strong></p>
</td>
<td width="276">
<p>&nbsp;&nbsp;&nbsp; Statement block</p>
</td>
</tr>
<tr>
<td width="247">
<p><strong>UNTIL</strong> condition p is true</p>
</td>
<td width="60">
<p>&nbsp;</p>
</td>
<td width="276">
<p><strong>ENDDO</strong></p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<h3>Counted Repetition</h3>
<p>Counted repetition occurs when the exact number of loop iterations is known in advance.&nbsp;The execution of the loop is controlled by a loop index.</p>
<p>&nbsp;</p>
<h3>General format:</h3>
<p><strong>DO</strong> loop-index = initial-value to final-value</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Statement block</p>
<p><strong>ENDDO</strong></p>
<p>&nbsp;</p>
<p>The DO loop does more than just repeat the statement block.&nbsp;</p>
<ul>
<li>The <strong>DO&hellip;ENDDO</strong> loop functions:&nbsp; <strong>&nbsp;</strong></li>
<li>Initializes the &ldquo;loop-index&rdquo; to the &ldquo;initial-value&rdquo;</li>
<li>Increments the &ldquo;loop-index&rdquo; by 1 for each pass through the loop</li>
<li>Tests the value of the &ldquo;loop-index&rdquo; at the beginning of each pass through the loop to ensure it is in the stated range of values</li>
<li>Ends the loop when the &ldquo;loop-index&rdquo; is greater than the &ldquo;final-value&rdquo;</li>
</ul>
<p>&nbsp;</p>
<p>&nbsp;</p>