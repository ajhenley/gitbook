#The Structure Theorem

###The Structure Theorem
The Structure Theorem states that a solution can consist of a combination of just three constructs. They are sequence, selection and repetition control structures. You can represent each control structure in pseudocode.

###Three control structures
####Sequence

The sequence control structure describes the linear execution of one step after another. In pseudocode, this construct is represented as a sequence of pseudocode statements:


statement a
statement b
statement c

A sequence of statements in an algorithm might read:

add 1 to pageCount
Print heading line1
Print heading line2
Set lineCount to zero
Read customer record

These instructions illustrate the sequence control structure as a list of steps. Each is written one after the other, from start to finish. Each instruction will be executed as it appears.

####Selection

The selection control structure presents an expression or condition as the choice between two actions. The choice depends on whether the expression evaluates to true or false. This construct represents the decision-making abilities of the computer. 

In pseudocode, selection is represented by the keywords IF,THEN,ELSE and ENDIF:

IF condition x is true THEN
    perform statement(s)in the true case
ELSE
    perform statement(s)in the false case
ENDIF

If the expression evaluates to true, then the statement(s) that follow the true case will be executed. The statements following the false case will not be executed.

In either case, control then passes to the next processing step after the delimiter ENDIF.

###A pseudocode example might read:
'''
IF employmentStatus is PART_TIME THEN
&nbsp;&nbsp;&nbsp;&nbsp;add 1 to partTimeCount
ELSE
&nbsp;&nbsp;&nbsp;&nbsp;add 1 to fullTimeCount
ENDIF
'''

####Repetition

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

 