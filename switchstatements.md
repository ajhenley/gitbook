###Switch statements
The switch statement allows your program to offer selection among different cases. The switch statement works with byte (or Byte), short (or Short), char (or Character), int (or Integer) and Strings.

The following code example, SwitchDemo, declares an int named month whose value represents a month. The code displays the name of the month, based on the value of month, using the switch statement.

````java
        //This program will print 'May' when you run it.
        int month = 5;
        String monthName;
        switch (month) {
            case 1:  monthName = "January";
                     break;
            case 2:  monthName = "February";
                     break;
            case 3:  monthName = "March";
                     break;
            case 4:  monthName = "April";
                     break;
            case 5:  monthName = "May";
                     break;
            case 6:  monthName = "June";
                     break;
            case 7:  monthName = "July";
                     break;
            case 8:  monthName = "August";
                     break;
            case 9:  monthName = "September";
                     break;
            case 10: monthName = "October";
                     break;
            case 11: monthName = "November";
                     break;
            case 12: monthName = "December";
                     break;
            default: monthName = "Unknown";
                     break;
        }
        System.out.println(monthName);
    ```
    
The default case should always go last.

You could also display the name of the month with if-then-else statements but you may find the switch statement to be more intuitive and readable.

An if-then-else statement can test expressions based on ranges of values or conditions. But a switch statement tests expressions based only on a single value.

Another point of interest is the break statement. Each break statement terminates the enclosing switch statement. Control flow continues with the first statement following the switch block. The break statements are necessary because without them, statements in switch blocks fall through: All statements after the matching case label are executed in sequence, regardless of the expression of subsequent case labels, until a break statement is encountered. 



####Your assignment
Write a program using a switch statement to print the month names given the number of days in the month. If the user enters 30 then the program will say: 
"Thirty days has September,April, June, and November"


