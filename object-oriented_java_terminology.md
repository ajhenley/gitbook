


Here are some of the basic building blocks of Objected-Oriented Programming that you will become familiar with:

class
    A collection of related fields (instance and class variables) and methods that have one purpose.
instance variable (aka field variable or member variable
    An instance variable is a variable that is defined in a class, but outside of a method. There is one copy of the variable for every instance (object) created from that class.

    A common problem is trying to reference an instance variable from a static method. A static method (eg, main) can only reference static variables in its own class (or its own local variables).
class variable (aka static variable)
    A class variable or static variable is defined in a class, but there is only one copy regardless of how many objects are created from that class. It's common to define static final variables (constants) that can be used by all methods, or by other classes. Color.blue is an example of a static final variable.
constructor
    A constructor is a method with the same name as the class. When an object is created, the constructor for that class is called. If no constructor is defined, a default constructor is called. It's common to have multiple constructors taking different numbers of parameters. Before a constructor is executed, the constructor for the parent class is called implicitly if there is no parent constructor called explicitly on the first line.
override (applies to methods)
    If a subclass redefines a method defined in a superclass, the method in the superclass is overridden.  The "super" keyword is how you refer to the overridden parent method. There is no way to explicitly call the "grandparent's" method if it was overridden by the parent class.
overload (applies to methods)
    A method in a class is overloaded if there is more than one method by the same name. If the same name is used, the methods must different in the number and/or types of the parameters so that there is no confusion. This really has nothing to do with classes, only methods.
abstract class
    A class which doesn't define all it's methods is called an abstract class. To be useful, there must be a subclass which defines the missing methods. The "You must declare this class abstract" error message from the Java compiler is rather misleading. This usually means that you declared your class to implement an interface, but failed to write all required methods -- or more commonly that there's a spelling error in a method header.
interface
    An interface is a list of methods that must be implemented. A class that implements an interface must define all those methods. The method signatures (prototypes) are listed in the interface. Interfaces may also define public static final "constants". An interface is essentially the same as an completely abstract class.



