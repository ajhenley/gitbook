# Bubble Sort

<h3><strong>Bubble Sort</strong></h3>
<p>The Bubble Sort algorithm considers each element in the list. When the algorithm finds two consecutive elements out of order, they are swapped. The result is a sorted list. 


The algorithm repeatedly traverses the unsorted part of the array, comparing consecutive elements. They are swapped using temporary variable when they are out of order. The name of the algorithm refers to the fact that the largest element "sinks" to the bottom and the smaller elements "float" to the top. The bubble sort will continue until the list is sorted and no swaps have occurred. 

Note that <b>a</b> is the list, <b>n</b> represents the number of elements in the list and <b>temp</b> represents the temporary (swap) variable.
<pre> 
For i = 0 to n - 1
    For j = 1 to n 
        If (a(j) &gt; a(j + 1))
            temp = a(j)
            a(j) = a(j + 1)
            a(j + 1) = temp
        End-If
    End-For
End-For
</pre>

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

Test the algorithm on an the following list: 1,2,3,4,5. What happens?

How would you change the algorithm to sort in descending order?


