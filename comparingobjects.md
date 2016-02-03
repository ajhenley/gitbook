###Comparing People
Today you're going to learn about comparing people. Yes, despite what your mother may have told you... there are lesser people and greater people. At least in this example. 

Let's start with a Person class... to keep our people simple we'll only include first name and last name. I'll let you add more features on your own.

{%ace edit=true, lang='java'%}
class Person {
	private String firstName;
	private String lastName;
	
    Person(String firstName,String lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }
    
    public String getFirstName() {
		return firstName;
	}

	public void setFirstName(String name) {
		this.firstName = name;
	}
	
	public void setLastName(String name) {
		this.lastName = name;
	}
	
    public String getLastName() {
		return lastName;
	}

    public String getFullName() {
    	return firstName + " " + lastName;
    }


    @Override
    public String toString() {
        return String.format("%s", getFullName());
    }
}
{%endace%}






What are Java Comparators and Comparables?

 

Comparable

A comparable object is capable of comparing itself with another object. The class itself must implements the java.lang.Comparable interface in order to be able to compare its instances.


Comparator

A comparator object is capable of comparing two different objects. The class is not comparing its instances, but some other class’s instances. This comparator class must implement the java.util.Comparator interface.


Do you need to compare objects?

TWhen there is a list of objects, ordering these objects into different orders often becomes a requirement. If you have of list of employee objects you may wish to sort them using the employee id, name or start date (length of employment).


