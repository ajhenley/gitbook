# Bubble Sort

<h3><strong>Bubble Sort</strong></h3>
<p>Suppose A is an array of N values. We want to sort A in ascending order.</p>
<p>Bubble Sort is a simple-minded algorithm based on the idea that we look at the list, and wherever we find two consecutive elements out of order, we swap them. We do this as follows: We repeatedly traverse the unsorted part of the array, comparing consecutive elements, and we interchange them when they are out of order. The name of the algorithm refers to the fact that the largest element "sinks" to the bottom and the smaller elements "float" to the top.</p>
<pre>     For I = 1 to N - 1
       For J = 1 to N - 1
         If (A(J) &gt; A(J + 1)
           Temp = A(J)
           A(J) = A(J + 1)
           A(J + 1) = Temp
         End-If
       End-For
     End-For</pre>
<p>Bubble Sort does roughly N**2 / 2 comparisons and does up to N**2 / 2 swaps.</p>