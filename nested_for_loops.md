<!--djw:done
todo: use an image for the table which doesn't line up well.

-->
###Nested for loops

A for loop inside a for loop is called a nested  for loop. Sometimes this is the right tool for the job. Here's an example where you print out a multiplication table. Notice that we set the Maximum number if iterations as a variable. You could even prompt the user for this value making the for loop even more flexible.


{%ace edit=true, lang='java'%}
Example: Print out the multiplication table.

public class MultiplicationTable {
  static final int MAX = 10;

  public static void main (String[] args) {
    int row, column;

    for (row = 1; row <= MAX; row++) {
      for (column = 1; column <= MAX; column++)
      {
          System.out.print(row * column + "\t");
      }
      System.out.println();//Takes us to the next line
    }
  }
}

{%endace%}

Table generated from the program
<pre>
1   2	3	4	5	6	7	8	9	10	
2	4	6	8	10	12	14	16	18	20	
3	6	9	12	15	18	21	24	27	30	
4	8	12	16	20	24	28	32	36	40	
5	10	15	20	25	30	35	40	45	50	
6	12	18	24	30	36	42	48	54	60	
7	14	21	28	35	42	49	56	63	70	
8	16	24	32	40	48	56	64	72	80	
9	18	27	36	45	54	63	72	81	90	
10	20	30	40	50	60	70	80	90	100	
</pre>


