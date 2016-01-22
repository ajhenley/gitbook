###Composition
In real-life, complex objects are often built from smaller, simpler objects. For example, a car contains a frame, an engine, tires, a transmission, a steering wheel, and a vast number of other parts. A personal computer contains a CPU, motherboard, memory, etc... Even you contain many smaller parts: you have a head, a body, legs, arms, and so on. Composition is process of building complex objects from simpler ones. This type of relationship is a containing relationship.

Composition is used for objects that have what we call a **has-a** relationship to each other. A car *has-a* metal frame, *has-an* engine, and *has-a* transmission. A personal computer *has-a* CPU, a motherboard, and other components. You *have-a* head, a body, some limbs.

The classes we have used so far have had member variables composed of existing data types (e.g. int, double, boolean). This may suffice for designing and implementing small, simple classes. It becomes burdensome for complex classes. Java allows us to build complex classes simply by using classes as member variables in other classes.

Java composition works by using instance variables that refer to other objects. A Person (object) *has a* Job (object). You'll find the Job object as a variable in the Person object below.

{%ace edit=true, lang='java'%}
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
{%endace%}

{%ace edit=true, lang='java'%}
//Person.java
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
{%endace%}

{%ace edit=true, lang='java'%}
//CompositionBasics.java
public class CompositionBasics {
    public static void main(String[] args) {
        Person bobby = new Person();
        System.out.println(bobby.getSalary());
    }

}
{%endace%}

Notice that above test program is not affected by any change in the Job object. If you are looking for code reuse and the relationship between two classes is *has-a* then you should use composition rather than inheritance.

The benefit of using composition is that we can control the visibility of other objects to client classes and reuse only what we need.

Also if there is any change in the other class implementation, for example getSalary returning String, we need to change Person class to accomodate it but client classes don’t need to change.

So composition allows creation of back-end class when it’s needed, for example we can change Person getSalary method to initialize the Job object.

What You Should Try Now
Create an Education class and make an instance of the Education class a member of the Person class. Your education class should include a list of last 10 schools attended.
Create a toString override for both Job and Education that outputs the information in the class to the console. The toString override for Person should use the toString methods for the Job and Education member objects.

