# Debugging Activity: Print Student Records

Chanchal is the project manager for a small software development project. She needs a weekly report of the employees who have worked on her project, separated by full-time and part-time.

She has developed the pseudocode below but since she is the project manager and not the programmer it has an error in it. It's your job to fix the error to make her look good to the team. She plans to present the report at the standing meeting tomorrow morning. If you succeed she will look good and remember you when assigning new tasks.

<li>a DOWHILE loop to control the repetition</li>
<li>An IF statement to select &lsquo;S&rsquo; records</li>
</ol>
<h3>Incorrect Results - find and fix the error</h3>

<pre>Print_student_records
Print &lsquo;Employee List&rsquo; heading
Read timesheet record
    DOWHILE morerecords exist
        IF timesheet_status = &lsquo;FT&rsquo; THEN
            Print EmployeeID, Department, Billing Rate, Hours Worked
        ENDIF
    ENDDO
    Read student record
END
</pre>
