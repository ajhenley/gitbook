###Comparing People
Today you're going to learn about comparing people. Yes, despite what your mother may have told you... there are lesser people and greater people. At least in this example. 

Let's start with a Person class... to keep our people simple we'll include just the first name and last name. Most people are more complex than that but I'll let you add more features on your own.

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

Next, try to sort the Person class. Can't do it. It won't work. It's not you. It's me. We're incompatible.

{%ace edit=true, lang='java'%}
//create a list of the Simpsons	characters
List<Person> simpsons = new ArrayList<Person>();
//Populate with our favorite cartoon TV characters
simpsons.add(new Person("Bart","Simpson"));
simpsons.add(new Person("Montgomery","Burns"));
simpsons.add(new Person("Waylon","Smithers"));
simpsons.add(new Person("Ned","Flanders"));
Collections.sort(simpsons);
{%endace%}


####Why? What can I do? Is there no hope?
The ```sort()``` method of the Collections class uses ```compareTo()``` to determine how the LIst or object array should be sorted. There is hope! Simply implement your own ```compareTo()``` method. Now you get to be the one who determines the criteria by which the classes will sort.

**Here's how to add CompareTo() to the Person class:**
{%ace edit=true, lang='java'%}
class Person implements Comparable<Person>{
	private String firstName;
	private String lastName;
	//<existing code not shown but you still need it>
	public int compareTo(Person p) {
	    return lastName.compareTo(p.getLastName());
	}
}
{%endace%}

Now you can sort the Person class with ```Collections.sort(simpsons);```



####What are Java Comparators and Comparables?
**Comparable**
A comparable object is capable of comparing itself with another object. The class itself must implements the ```java.lang.Comparable``` interface in order to be able to compare its instances.

**Comparator**
A comparator object is capable of comparing two different objects. The class is not comparing its instances, but some other class’s instances. This comparator class must implement the ```java.util.Comparator``` interface.

####Do you need to compare objects?
If you have of list of Simpson character objects you may wish to sort them using the last name or some other field. This is a common requirement when working with Simpsons or other objects that might like to be sorted.




