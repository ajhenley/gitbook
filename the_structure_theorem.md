#The Structure Theorem

###The Structure Theorem
The Structure Theorem states that a computer program can be constructed using just sequence, selection or repetition control structures. Each control structure is easily represented in pseudocode.

####The three basic control structures
#####Sequence

The sequence control structure is the straightforward execution of one processing step after another. In pseudocode, this construct is represented as a sequence of pseudocode statements:


statement a<br/>
statement b<br/>
statement c


For example, a typical sequence of statements in an algorithm might read:

add 1 to pageCount<br/>
Print heading line1<br/>
Print heading line2<br/>
Set lineCount to zero<br/>
Read customer record<br/><br/>
These instructions illustrate the sequence control structure as a straightforward list of steps written one after the other, in a top-to-bottom
fashion. Each instruction will be executed in the order in which it appears.

#####Selection

The selection control structure presents and expression or condition as the choice between two actions. The choice depends on whether the expression evaluates to true or false. This construct represents the decision-making abilities of the computer. 

In pseudocode, selection is represented by the keywords IF,THEN,ELSE and ENDIF:

IF condition p is true THEN<br/>
&nbsp;&nbsp;&nbsp;&nbsp;statement(s)in true case<br/>
ELSE<br/>
&nbsp;&nbsp;&nbsp;&nbsp;statement(s)in false case<br/>
ENDIF<br/><br/>

If the expression evaluates to true, then the statement(s) that follow the true case will be executed. And the statements following the false case will not be executed. Otherwise (the ELSE statement) the statements in the true case will be skipped and statements in the false case will be executed. In either case, control then passes to the next processing step after the delimiter ENDIF.

###A typical pseudocode example might read:

IF student_attendance_status is part_time THEN<br/>
&nbsp;&nbsp;&nbsp;&nbsp;add 1 to part_time_count<br/>
ELSE<br/>
&nbsp;&nbsp;&nbsp;&nbsp;add 1 to full_time_count<br/>
ENDIF
 

##### Repetition

The repetition control structure can be defined as the presentation of a set of instructions to be performed repeatedly, as long as a condition is true. The basic idea of repetitive code is that a block of statements is executed again and again, until a terminating condition occurs. This construct represents the sixth basic computer operation, namely to repeat a group of actions.

It is written in pseudocode as:

DOWHILE condition p is true<br/>
&nbsp;&nbsp;&nbsp;&nbsp;statement block<br/>
ENDDO<br/><br/>

The DOWHILE loop is a leading decision loop; that is, the condition is tested before any statements are executed. If the condition in the DOWHILE statement is found to be true, the block of statements following that statement is executed once. The delimiter ENDDO then triggers a return of control to the retesting of the condition. If the condition is still true, the statements are repeated, and so the repetition process continues until the condition is found to be false.

Control then passes to the statement that follows the ENDDO statement.It is imperative that at least one statement within the statement block alters the condition and eventually renders it false, because otherwise the logic may result in an endless loop.

Here is a pseudocode example that represents the repetition control structure:

Set student_total to zero
DOWHILE student_total < 50<br/>
&nbsp;&nbsp;&nbsp;&nbsp;Read student record<br/>
&nbsp;&nbsp;&nbsp;&nbsp;Print student name, address to report<br/>
&nbsp;&nbsp;&nbsp;&nbsp;add 1 to student_total<br/>
ENDDO<br/><br/>
 

###This example illustrates a number of points:

* The variable student_total is initialized before the DOWHILE condition is executed.
* As long as student_total is less than 50 (that is, the DOWHILE condition is true), the statement block will be repeated.
* Each time the statement block is executed,one instruction within that block will cause the variable student_total to be incremented.
* After 50 iterations, student_total will equal 50, which causes the DOWHILE condition to become false and the repetition to cease.
* It is important to realize that the initializing and subsequent incrementing of the variable tested in the condition is an essential feature of the DOWHILE construct.

 