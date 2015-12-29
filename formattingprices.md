###Formatting prices with two decimal places
You can use the NumberFormat class from the Java API
```java
NumberFormat nf = NumberFormat.getInstance();
nf.setMaximumFractionDigits(2);
nf.setMinimumFractionDigits(2);
setRoundingMode(RoundingMode.HALF_UP);

System.out.print(nf.format(decimalNumber));
```

Or you can use String.format. This will also work with printf to print a formatted string.

```java
double myDouble = 3.5;
String formattedData = String.format(%.02f",myDouble);
```

