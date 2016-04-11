<!--ajh:done-->
The **NumberFormat** class helps you to format and parse numbers or currency values. Since it's an abstract class you must call the ```getInstance()``` method or some variation of that method.
 
{%ace edit=false, lang='java'%}
myString = NumberFormat.getInstance().format(myNumber);
{%endace%}

###Formatting prices with two decimal places
You can use the NumberFormat class from the Java API

{%ace edit=false, lang='java'%}
NumberFormat nf = NumberFormat.getInstance();
nf.setMaximumFractionDigits(2);
nf.setMinimumFractionDigits(2);
setRoundingMode(RoundingMode.HALF_UP);

System.out.print(nf.format(decimalNumber));
{%endace%}

Or you can use String.format. This will also work with printf to print a formatted string.

{%ace edit=false, lang='java'%}
double myDouble = 3.5;
String formattedData = String.format("%.02f",myDouble);
{%endace%}
