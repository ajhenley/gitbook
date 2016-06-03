# Multidimentional Arrays

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