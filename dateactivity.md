###Date activity
Write an application to tell the user about a day in the past (their birthday, the Battle of Normandy, the date of their first drink etc.). It should keep asking until the user enters an empty date. The interaction should look something like this:

What is the date that you are asking about?    :  9/27/70
That was a Saturday. It was a sunny day and the temperature averaged 78 degrees. It was 23000 days ago.
What is the date that you are asking about?    :  
You can randomly generate the text about the weather and temperature that day, but you should know enough by now to accurately identify the day of the week and the number of days between that day and the current date.

####Helpful Hint
First create a class that given a date has a method stub to return the output sentence.
Next, create methods stubs to find the day of the week, the number of days, the weather and the temperature.
One by one, fill in those method stubs to make them operational.

####Bonus (Die with the Lie) 
Have the application give consistent information about the weather and temperature. If the application is asked about a date that it has already been asked about that run, it should give the same answer.
