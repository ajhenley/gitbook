# Searching and Printing an Array

###Searching an array
* A linear search of an array (look at each element starting with first)

###Linear search of an array
<pre>Linear_search_of_an_array
   Set max_num_elements to required value
   Set element_found to false
   Set index to 1

   DOWHILE(NOT element_found)AND(index &lt;= max_num_elements)
        IF array(index)= input_value THEN
          Set element_found to true
        ELSE
	      index = index + 1
        ENDIF
   ENDDO

   IF element_found THEN
       Print array (index)
   ELSE
       Print &lsquo;value not found&rsquo;, input_value
   ENDIF
END
</pre>
###Binary search of an array
* faster than linear search for arrays with &gt; 25 elements
* first, sort elements into ascending sequence
* next, locate the middle element
* then determine if your element is in the first half or second
* repeat the process with the selected half of the array

<pre>Binary_search_of_an_array

   Set element_found to false
   Set low_element to 1
   Set high_element to max_num_elements

   DOWHILE (NOT element_found)
                AND(low_element &lt;= high_element)
       index = (low_element + high_element)/2
	   
       IF input_value = array (index)THEN
          Set element_found to true
       ELSE
          IF input_value &lt; array (index)THEN
              high_element = index &ndash; 1
          ELSE
              low_element = index + 1
          ENDIF
       ENDIF
   ENDDO

IF element_found THEN
       Print array (index)
   ELSE
       Print &lsquo;value not found&rsquo;, input_value
   ENDIF
END
</pre>
<h3>Writing out contents of an array</h3>
<ul>
<li>use DO loop</li>
<li>start with first element</li>
<li>write each element until done</li>
</ul>
<pre>Write_values_of_array
     DO index = 1 to number_of_elements
          Print array(index)
     ENDDO
END
</pre>