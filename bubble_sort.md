# Bubble Sort

<h3><strong>Bubble Sort</strong></h3>
<p>The Bubble Sort algorithm considers each element in the list. When the algorithm finds two consecutive elements out of order, they are swapped. The result is a sorted list. 


The algorithm repeatedly traverses the unsorted part of the array, comparing consecutive elements. They are swapped using temporary variable when they are out of order. The name of the algorithm refers to the fact that the largest element "sinks" to the bottom and the smaller elements "float" to the top.

Note that N represents the number of elements in the list and temp represents the temporary (swap) variable.
<pre> 
For I = 0 to N
    For J = 1 to N - 1
        If (A(J) &gt; A(J + 1))
            temp = A(J)
            A(J) = A(J + 1)
            A(J + 1) = temp
        End-If
    End-For
End-For
</pre>
<p>Bubble Sort does roughly N**2 / 2 comparisons and does up to N**2 / 2 swaps.</p>

Test the bubble sort algorithm by having it sort the letters in your first and last name.

Next sort the following numbers: 34,29,69,33,88,2,43,0,94.

Finally sort the Presidents (since Kennedy) by last name:
35. John F. Kennedy (1961-1963)
36. Lyndon B. Johnson (1963-1969)
37. Richard Nixon (1969-1974)
38. Gerald Ford (1974-1977)
39. Jimmy Carter (1977-1981)
40. Ronald Reagan (1981-1989)
41. George Bush (1989-1993)
42. Bill Clinton (1993-2001)
43. George W. Bush (2001-2009)
44. Barack Obama (2009-present)

How would you change the algorithm to sort in descending order?


