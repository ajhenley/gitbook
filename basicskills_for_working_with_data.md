###Basic Skills for Working with Data

####The Eight Primitive Data Types
Type	Bytes	Use
byte	1	Very short integers from -128 to 127.
short	2	Short integers from -32,768 to 32,767.
int	4	Integers from -2,147,483,648 to 2,147,483,647
long	8	Long integers from -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807
float	4	Single-recision, floating-point numbers from -1.7E308 to 1.7E308 with up to 16 significant digits.
char	2	A single Unicode character that's stored in two bytes.
boolean	1	A true or false value.
How to declare and initialize a variable in two statements

Syntax:
{%ace edit=true, lang='java'%}
type variableName.
variableName = value;
{%endace%}

Example:
{%ace edit=true, lang='java'%}
int counter;
counter = 1;
{%endace%}
How to declare and initialize a variable in one statement

Syntax:
{%ace edit=true, lang='java'%}
int counter = 1;
{%endace%}

Examples:
{%ace edit=true, lang='java'%}
double price = 14.95;
float interestRate = 8.125F;
long numberOfBytes = 2000L;
int population = 1734323;
int popluation = 1_734_423;
double distance = 3.65e+9;
char letter = 'A';
char letter = 65;
boolen valid = false;
int x = 0, y = 0;
{%endace%}
A variable stores a value that can change as a program executes.
Before you can use a variable, you must declare its data type and initialize it by assigning a value to it.

To declare and initialize more than one variable for a single data type in a single statement, use commas to seperate the assignments.
To identify float values, you must type an f or F after the number. To identify long values, you must type an l or L after the number.
