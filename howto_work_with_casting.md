###How to Work with Casting
As you continue to work with Java programs, you will frequently need to convert data from one data type to another. To do that, you use a technique called casting. It'summarized below:

####How Implicit Casting Works
Casting from less precise to more precise data types
```byte --> short --> int --> long --> float --> double```

####Examples
{%ace edit=true, lang='java'%}
double grade = 93;

double d = 95.0;
int i = 86; j = 91;
double average = (d+i+j)/3;
{%endace%}

You will always be able to use less precise literals, variables or constants in equations that assign values to a more precise type. This is called implicit casting.

####How to Code an Explicit Cast

####Syntax:
```(type) expression```

####Examples:
{%ace edit=true, lang='java'%}
int grade = (int) 93.75;

double d = 95.0;
int i = 86; j = 91;
double average = ((int) d + i + j)/3;

double result = (double) i / (double) j;
{%endace%}
An explicit cast requires you to indicate to the compiler exactly what values in an expression you want converted.

####How to cast between char and int types
{%ace edit=true, lang='java'%}
char letterChar = 65; 
char letterChar2 = (char) 65;
int letterInt = "A";
int letterInt2 = ( int ) 'A';
{%endace%}