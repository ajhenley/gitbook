# Naming Conventions

When designing a solution algorithm the programmer will introduce some unique names to be used to represent the variables or objects in the problem. All names should be meaningful. A name given to a variable is simply a method of identifying a particular storage location in the computer.

The uniqueness of a name will differentiate this location from others. Often a name describes the type of data stored in a particular variable. For instance, a variable may be one of three simple data types: an integer, a real number or a character. The name itself should be transparent enough to adequately describe the variable; for example, number1, number2 and number3 are more meaningful names for three numbers than A, B and C. But taxRate, income, and nmbrDependents are more meaningful still.

If more than one word is used in the name of a variable, then underscores are useful as word separators, for example sales_tax and word_count. If an underscore is not desirable, then words can be joined together with the use of a capital letter as a word separator, for example salesTax and wordCount. The latter is more common and is known as Camel Case.

Most programming languages do not tolerate a space in a variable name, as a space would signal the end of the variable name and thus imply that there were two variables. 

For readability, it is not advisable to string together words all in lower case. A name such as ‘carregistration’ is much harder to read than
‘carRegistration’.

 

How this applies to Java ... 

Naming Conventions
A well-written program should be self-documenting. Naming conventions make programs more understandable by making them easier to read.  They can also give information about the function of the identifier-for example, whether it's a constant, package, or class-which can be helpful in understanding the code.

| 0:0 | 1:0 |
| -- | -- |
| 0:2 | 1:2 |

{|
|-
|Identifier Type
|Rules for Naming
|Examples
|Packages
|The prefix of a unique package name is always written in all-lowercase ASCII letters and should be one of the top-level domain names, currently com, edu, gov, mil, net, org, or one of the English two-letter codes identifying countries as specified in ISO Standard 3166, 1981.
|-
Subsequent components of the package name vary according to an organization's own internal naming conventions. Such conventions might specify that certain directory name components be division, department, project, machine, or login names.
|-
com.sun.eng
com.apple.quicktime.v2
edu.cmu.cs.bovik.cheese
|}

Classes


Class names should be nouns, in mixed case with the first letter of each internal word capitalized. Try to keep your class names simple and descriptive. Use whole words-avoid acronyms and abbreviations (unless the abbreviation is much more widely used than the long form, such as URL or HTML).


class Raster; 
class ImageSprite;


Interfaces


Interface names should be capitalized like class names.


interface RasterDelegate; 
interface Storing;


Methods


Methods should be verbs, in mixed case with the first letter lowercase, with the first letter of each internal word capitalized.


run(); 
runFast(); 
getBackground();


Variables


Except for variables, all instance, class, and class constants are in mixed case with a lowercase first letter. Internal words start with capital letters. Variable names should not start with underscore _ or dollar sign $ characters, even though both are allowed.

Variable names should be short yet meaningful. The choice of a variable name should be mnemonic- that is, designed to indicate to the casual observer the intent of its use. One-character variable names should be avoided except for temporary "throwaway" variables. Common names for temporary variables are i, j, k, m, and n for integers; c, d, and e for characters.



int             i;
char            c;
float           myWidth;

Constants


The names of variables declared class constants and of ANSI constants should be all uppercase with words separated by underscores ("_"). (ANSI constants should be avoided, for ease of debugging.)


static final int MIN_WIDTH = 4;

static final int MAX_WIDTH = 999;

static final int GET_THE_CPU = 1;