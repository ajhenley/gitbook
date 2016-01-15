# Inheritence and constructors

Constructors are not inherited. If we add a constructor to the Employee class, our subclasses do not compile.  The error:
```
Lawyer.java:2: cannot find symbol
symbol  : constructor Employee()
location: class Employee
public class Lawyer extends Employee {
       ^
```
The short explanation: Once we write a constructor (that requires parameters) in the superclass, we must now write constructors for our employee subclasses as well.



Subclasses don't inherit the Employee(int) constructor.

Subclasses receive a default constructor that contains:

public Lawyer() {
    super();       // calls Employee() constructor
}


But our Employee(int) replaces the default Employee().
The subclasses' default constructors are now trying to call a non-existent default Employee constructor.


super(parameters);


Example:
	public class Lawyer extends Employee {
	    public Lawyer(int years) {
	        super(years);  // calls Employee c'tor
	    }
	    ...
	}

The super call must be the first statement in the constructor.
	
	

Inheritance and constructors
•If we add a constructor to the Employeeclass, our subclasses do not compile.  The error:
Lawyer.java:2: cannot find symbol symbol  : constructor Employee() location: class Employee public class Lawyer extends Employee {
^
•The short explanation: Once we write a constructor (that requires parameters) in the superclass, we must now write constructors for our employee subclasses as well.
