###Composition
In real-life, complex objects are often built from smaller, simpler objects. For example, a car is built using a metal frame, an engine, some tires, a transmission, a steering wheel, and a large number of other parts. A personal computer is built from a CPU, a motherboard, some memory, etc… Even you are built from smaller parts: you have a head, a body, some legs, arms, and so on. This process of building complex objects from simpler ones is called composition (also known as object composition).

More specifically, composition is used for objects that have a **has-a** relationship to each other. A car *has-a* metal frame, *has-an* engine, and *has-a* transmission. A personal computer *has-a* CPU, a motherboard, and other components. You have-a head, a body, some limbs.

All of the classes we have used so far have had member variables composed of existing data types (e.g. int, double, String). This may suffice for designing and implementing small, simple classes. It becomes burdensome for complex classes. Especially those built from lots of sub-parts. To facilitate the building of complex classes from simpler ones, Java allows object composition in a simple way. By using classes as member variables in other classes.

Java composition works by using instance variables that refers to other objects. A Person (object) *has a* Job (object). You'll find the Job object as a variable in the Person object below.

//Job.java
public class Job {
    private String role;
    private long salary;
    private int id;
         
    public String getRole() {
        return role;
    }
    public void setRole(String role) {
        this.role = role;
    }
    public long getSalary() {
        return salary;
    }
    public void setSalary(long salary) {
        this.salary = salary;
    }
    public int getId() {
        return id;
    }
    public void setId(int id) {
        this.id = id;
    }
}
Person.java

public class Person {
    //composition has-a relationship
    private Job job;
    
    public Person(){
        this.job=new Job();
        job.setSalary(1000L);
    }
    public long getSalary() {
        return job.getSalary();
    }
}
CompositionBasics.java

public class CompositionBasics {
    public static void main(String[] args) {
        Person bobby = new Person();
        System.out.println(bobby.getSalary());
    }

}
Github Repository (Links to an external site.)
Notice that above test program is not affected by any change in the Job object. If you are looking for code reuse and the relationship between two classes is has-a then you should use composition rather than inheritance.

The benefit of using composition is that we can control the visibility of other objects to client classes and reuse only what we need.

Also if there is any change in the other class implementation, for example getSalary returning String, we need to change Person class to accomodate it but client classes don’t need to change.

So composition allows creation of back-end class when it’s needed, for example we can change Person getSalary method to initialize the Job object.

What You Should Try Now

Create an Education class and make an instance of the Education class a member of the Person class. Your education class should include a list of last 10 schools attended.
Create a toString override for both Job and Education that outputs the information in the class to the console. The toString override for Person should use the toString methods for the Job and Education member objects.

