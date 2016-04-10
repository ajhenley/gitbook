<!--djw:done-->
It seems that Professor Strongheim can't easily compute GPAs accurately. The professor needs to store the relative weights of the different types of assignments in a database table. This should allow him to change the weights at will and then recompute the grades of his students.

####Example
The following table demonstrates how Porfessor Strongheim computes his grades. He takes the  percentage in each category and multiplies it by its respective weight. The sum of these contributions is the total grade percentage.

<table border='1'>
<tr><th>Category Name</th><th>Percentage in Category</th><th>*</th><th>Weight of Category</th><th>=</th><th>Contribution</th></tr>
<tr><td>Homework</td><td>93%</td><td>*</td><td>.30</td><td>=</td><td>0.279</td></tr>
<tr><td>Quiz/Test</td><td>88%</td><td>*</td><td>.50</td><td>=</td><td>0.440</td></tr>
<tr><td>Exam</td><td>91%</td><td>*</td><td>.20</td><td>=</td><td>0.182</td></tr>
<tr><td colspan="4">Total 90.1%</td></tr>
</table>

 Mathematically this problem can then be solved as follows.

h*(the weight of h) + q*(the weight of q) + e*(the weight of e) = final grade

As long as you're making changes allow the application to handle students in different classes. Some students in Professor Strongheim's 9:30 Earth Science class are also in his 1 pm Intro to Physics class. You need to ensure the Professor doesn't  mix the grades between those two classes.