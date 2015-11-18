# Change Activity: Process Student Records

<h2>Print selected students</h2>
<p>Design a solution algorithm that will read the student file and produce a report of all female students who are enrolled part-time. The report is to be headed &lsquo;FEMALE PART-TIME STUDENTS&rsquo; and is to show the student&rsquo;s number, name, address&nbsp; and age.</p>
<h2>A.&nbsp;&nbsp;&nbsp;&nbsp; Defining diagram</h2>
<p>&nbsp;<img src="/courses/970783/files/37087912/preview" alt="2.8.png" data-api-endpoint="https://canvas.instructure.com/api/v1/courses/970783/files/37087912" data-api-returntype="File" /></p>
<h2>B.&nbsp;&nbsp;&nbsp;&nbsp; Control structures required</h2>
<h2>C.&nbsp;&nbsp;&nbsp;&nbsp; Incorrect Results&hellip; find and fix the error</h2>
<p>&nbsp;</p>
<pre>Produce_part_time_female_list
	Print &lsquo;FEMALE PART-TIME STUDENTS&rsquo; heading
	Read student record
	DOWHILE more records
		IF student record = &lsquo;S&rsquo; record THEN
			IF attendance_pattern = F/T THEN
				Print student_number, name, address, age
			ENDIF
		ENDIF
		Read student  record
	ENDDO
END
</pre>