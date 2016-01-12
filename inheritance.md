###Inheritance
Let's talk about another key concept from object-oriented programming.
Inheritance: Forming new classes based on existing ones.


Inheritence gives us a way to share/reuse code between two or more classes. And code reuse means you don't have to write as much code which means development time is faster. This makes the project manager happy.

Inheritence means there's a parent class being extended. That's called the superclass.
We'll also have a child class that inherits behavior from superclass. The child class is called the subclass.
gets a copy of every field and method from superclass

is-a relationship: Each object of the subclass also "is a(n)" object of the superclass and can be treated as one.


	public class name extends superclass {

Example:

	public class Lawyer extends Employee {
	    ...
	}

By extending Employee, each Lawyer object now:
receives a copy of each method from Employee automatically
can be treated as an Employee by client code

Lawyer can also replace ("override") behavior from Employee.


override: To write a new version of a method in a subclass that replaces the superclass's version.
No special syntax required to override a superclass method.Just write a new version of it in the subclass.

	public class Lawyer extends Employee {
	    // overrides getVacationForm in Employee class
	    public String getVacationForm() {
	        return "pink";
	    }
	    ...
	}

A subclass can call its parent's method/constructor:

	super.method(parameters)  	// methodsuper(parameters);	      	// constructor



	public class Lawyer extends Employee {
      public Lawyer(String name) {
          super(name);
      }

	    // give Lawyers a $5K raise (better)
	    public double getSalary() {
	        double baseSalary = super.getSalary();
	        return baseSalary + 5000.00;
	    }
	}

public class Employee {
    private double salary;
    ...
}

public class Lawyer extends Employee {
    ...
    public void giveRaise(double amount) {
        salary += amount;   // error; salary is private
    }
}

Inherited private fields/methods cannot be directly accessed by subclasses.   (The subclass has the field, but it can't touch it.)
How can we allow a subclass to access/modify these fields?


protected type name;  	// field

protected type name(type name, ..., type name) {
    statement(s);     	// method
}

a protected field or method can be seen/called only by:
the class itself,  and its subclasses
also by other classes in the same "package"  (discussed later)
useful for allowing selective access to inner class implementation


public class Employee {
    protected double salary;
    ...
}

If we add a constructor to the Employee class, our subclasses do not compile.  The error:

Lawyer.java:2: cannot find symbol
symbol  : constructor Employee()
location: class Employee
public class Lawyer extends Employee {
       ^

The short explanation: Once we write a constructor (that requires parameters) in the superclass, we must now write constructors for our employee subclasses as well.


Constructors are not inherited.
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
