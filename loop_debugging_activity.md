# Loop debugging activity

<p>The following program is supposed to allow the user to input as many things as they want until they stop. Each time it is supposed to repeat what the user said, can you fix it?</p>

```java
import java.util.Scanner;

public class EndlessStrings {
    public void main (String[] args)
    {
        Scanner keyboard = new Scanner(System.in);
        
        String userInput = "";
        
        userInput = keyboard.next();
        
        while ( userInput != "" )
        {
            System.out.println(userInput);
            
        }
    }
}
```