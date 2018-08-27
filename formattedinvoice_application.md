###Formatted Invoice Application

<!--djw: has some text formatting issues-->
####The NumberFormat class

```java
java.text.NumberFormat
```

####Three static methods of the NumberFormat class

```java
getCurrencyInstance()
getPercentInstance()
getNumberInstance()
```

####Three methods of a NumberFormat object

```java
format(anyNumberType)
setMinimumFractionDigits(int)
setMaximumFractionDigits(int)
``` 

####The currency format

{%ace edit=true, lang='java'%}
double price = 11.575;
NumberFormat currency = NumberFormat.getCurrencyInstance();
String priceString = currency.format(price); // returns $11.58
The percent format
double majority = .505;
NumberFormat percent = NumberFormat.getPercentInstance();
String majorityString = percent.format(majority); // returns 50%
{%endace%}

####Your Assignment
Take the Line Item Invoice application that you created earlier and make the following changes: Use Formatted Output for the dollar amounts and quantities.