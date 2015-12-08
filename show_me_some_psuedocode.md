# Show Me Some Psuedocode!

Nothing teaches like a good example, right?

helps decrease the gap between developers and non-technical guys on a project, so you can make sure that the software will match the customers expectations.


Here is a complete example of a modular program using pseudocode.

####The problem
Your client requests a program that will print the weekly timesheet report. The project manager (client) needs to log on to the timekeeping system every week and download the report. The report contains all the employees. The timesheet report is not filtered by the particular project. Employees charge their hours to each project. This allows the program to exclude records for other projects.

####External to your program:
The project manager will log in to the timekeeping system and download a .csv file of all the hours charged by all employees for the week. The .csv will contain each employee number, name # hours, billing rate, project number for all charges for the week. The project manager will save this .csv file to a known directory.

####The Algorithm

####Inputs, Processing Steps, Outputs
Inputs|Processing Steps|Outputs
--|--|--
.csv file of all hours for all projects|print header<br>read file |write to output file


####Your program
You shall write a program which will prompt the project manager to enter the project number for the current project.
Then open up the .csv file and loop through each line. 
If the project number is the one entered then add that line to the final report. You shall extract the number, name, hours,  rate and calculate total hours. Write each employee line to the to a file, also .csv which will open in Excel.
<pre>Print_weekly_report
Begin
declare TotalPay = 0.0
prompt for CurrentProjectNumber
prompt for inputFilename
prompt for outputFilename
open inputFilename
printHeader(CurrentProjectNumber)
DO while not EOF
    if projectNumber = CurrentProjectNumber then
        read  employeeNumber, employeeName, hoursBilled, hourlyRate
        TotalPay = TotalPay + printWeeklyReport(employeeNumber,employeeName,hoursBilled,hourlyRate)
    end if
 

LOOP
printFooter
close input_filename
close output_filename
END</pre>

<pre>printWeeklyReport(employeeNumber,employeeName,hoursBilled,hourlyRate)
    weeklyPay = calculateWeeklyPay(hoursBilled,hourlyRate)
        write to output_filename employeeNumber, employeeName, weeklyPay
        return weeklyPay
</pre>
<pre>calculateWeeklyPay(hoursBilled,hourlyRate)
    return hoursBilled * hourlyRate
</pre>

<pre>printHeader(CurrentProjectNumber)
    print "Weekly Report for " + CurrentProjectNumber to outputFilename
</pre>    

<pre>printFooter(totalHours)
    
</pre>