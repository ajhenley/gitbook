# Multidimensional Arrays
An array can not only contain elements but also each element of an array could be ... another array! You've actually seen this. Lots of times, I bet. Have you worked in Excel before? Think of the first array as being the rows. And each row contains an array of columns. So if you stored your Student Gradebook in an Excel worksheet you would have an array of records (each student) and each student would contain four columns: gender, major, state, average score.

Your array would look like this:
<table>
<tr><td>M</td><td>Econ</td><td>MD</td><td>99</td></tr>
<tr><td>F</td><td>Mktg</td><td>VA</td><td>89</td></tr>
<tr><td>F</td><td>Biology</td><td>NJ</td><td>100</td></tr>
</table>

*... continues for 97 more rows...*

In Java, you could create this same structure as follows. This allows fast-progarmmatic access to your data using two dimensions. Think of the as the row index (or the index of the first array). And the column index (or the index of the second array).

You can access the elements of a two-dimensional array with two nested for-loops.

```java
public class MultiDimArrayDemo {
    public static void main(String[] args) {
    	
    	//array of gender, major, state, score
        String[][] studentGradebook = new String[100][4];
      
        studentGradebook[0][0] = "M";
        studentGradebook[0][1] = "Econ";
        studentGradebook[0][2] = "MD";
        studentGradebook[0][3] = "99";

        studentGradebook[1][0] = "F";
        studentGradebook[1][1] = "Mktg";
        studentGradebook[1][2] = "VA";
        studentGradebook[1][3] = "89";
        
        studentGradebook[2][0] = "F";
        studentGradebook[2][1] = "Biology";
        studentGradebook[2][2] = "NJ";
        studentGradebook[2][3] = "100";
        
        for (int i = 0; i < 3; i++)
        {
        	for (int j = 0; j < 4; j++)
            {
        	System.out.println(studentGradebook[i][j]);
            }
        }
        
    }
}
```