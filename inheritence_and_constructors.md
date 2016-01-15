####Inheritence and constructors
* Every class (including abstract classes) must have a constructor.
* If you don't type the constructor, Java will create one for you
* Constructors are the code that runs when you use the keyword ```new```
* Constructors do not have return types; they are not methods
* It's common to have a no-argument constructor
* You can also create a constructor that takes parameters
* 

####Do constructors get inherited?
Constructors are not inherited. If we add a constructor to the Employee class, our subclasses do not compile.  The error:
```
Lawyer.java:2: cannot find symbol
symbol  : constructor Employee()
location: class Employee
public class Lawyer extends Employee {
       ^
```
The short explanation: Once you write a constructor that requires parameters in the superclass, you must now write constructors for your subclasses as well.

Subclasses don't inherit the Employee(int) constructor.
Subclasses receive a default constructor that contains a call to the superclass's constructor. If you don't program this then Java will.

{%ace edit=true, lang='java'%}
public Lawyer() {
    super();       // calls Employee() constructor
}
{%endace%}
**The super call must be the first statement in the constructor.**

A constructor that takes arguments replaces the default constructor.
But our Employee(int) replaces the default Employee().

The subclasses' default constructors are now trying to call a non-existent default Employee constructor.

super(parameters);
{%ace edit=true, lang='java'%}
	public class Lawyer extends Employee {
	    public Lawyer(int years) {
	        super(years);  // calls Employee c'tor
	    }
	    ...
	}
{%endace%}




Inheritance and constructors
•If we add a constructor to the Employeeclass, our subclasses do not compile.  The error:
Lawyer.java:2: cannot find symbol symbol  : constructor Employee() location: class Employee public class Lawyer extends Employee {
^
•The short explanation: Once we write a constructor (that requires parameters) in the superclass, we must now write constructors for our employee subclasses as well.
