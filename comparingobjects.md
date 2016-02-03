# Comparing Objects

What are Java Comparators and Comparables?

 

Comparable

A comparable object is capable of comparing itself with another object. The class itself must implements the java.lang.Comparable interface in order to be able to compare its instances.


Comparator

A comparator object is capable of comparing two different objects. The class is not comparing its instances, but some other class’s instances. This comparator class must implement the java.util.Comparator interface.


Do you need to compare objects?

TWhen there is a list of objects, ordering these objects into different orders often becomes a requirement. If you have of list of employee objects you may wish to sort them using the employee id, name or start date (length of employment).


The Java API contains to methods which support comparison, and each of these has one method to be implemented by the user.


java.lang.Comparable: int compareTo(Object o1)
This method compares this object with o1 object. Returned int value has the following meanings.

positive – this object is greater than o1
zero – this object equals to o1
negative – this object is less than o1

java.util.Comparator: int compare(Object o1, Objecto2)
This method compares o1 and o2 objects. Returned int value has the following meanings.

positive – o1 is greater than o2
zero – o1 equals to o2
negative – o1 is less than o2

java.util.Collections.sort(List) and java.util.Arrays.sort(Object[]) methods can be used to sort using natural ordering of objects.
java.util.Collections.sort(List, Comparator) and java.util.Arrays.sort(Object[], Comparator) methods can be used if a Comparator is available for comparison.

The Employee example is a good candidate for explaining these two concepts. First create a simple Java class to represent the Employee.


public class Employee {
private int empId;
private String name;
private int age;

public Employee(int empId, String name, int age) {
// set values on attributes
}
// getters & setters
}

Next create a list of Employees for using in different sorting requirements. Employees are added to a List without any specific order in the following class.


import java.util.*;

public class Util {

public static List<Employee> getEmployees() {

List<Employee> staff = new ArrayList<Employee>();

col.add(new Employee(5, "Frank", 28));
col.add(new Employee(1, "Jorge", 19));
col.add(new Employee(6, "Bill", 34));
col.add(new Employee(3, "Michel", 10));
col.add(new Employee(7, "Simpson", 8));
col.add(new Employee(4, "Clerk",16 ));
col.add(new Employee(8, "Lee", 40));
col.add(new Employee(2, "Mark", 30));

return staff; 
}
 }
 

Sorting in natural ordering

Employee’s natural ordering would be done according to the employee id. For that, above Employee class must be altered to add the comparing ability as follows.


public class Employee implements Comparable<Employee> {
private int empId;
private String name;
private int age;

/**
* Compare a given Employee with this object.
* If employee id of this object is 
* greater than the received object,
* then this object is greater than the other.
*/
public int compareTo(Employee o) {
return this.empId - o.empId ;
}
….
}

The new compareTo() method does the trick of implementing the natural ordering of the instances. So if a collection of Employee objects is sorted using Collections.sort(List) method; sorting happens according to the ordering done inside this method.

We’ll write a class to test this natural ordering mechanism. Following class use the Collections.sort(List) method to sort the given list in natural order.


import java.util.*;

public class TestEmployeeSort {

public static void main(String[] args) {     
List coll = Util.getEmployees();
Collections.sort(coll); // sort method
printList(coll);
}

private static void printList(List<Employee> list) {
System.out.println("EmpId\tName\tAge");
for (Employee e: list) {
System.out.println(e.getEmpId() + "\t" + e.getName() + "\t" + e.getAge());
}
}
}

Run the above class and examine the output. It will be as follows. As you can see, the list is sorted correctly using the employee id. As empId is an int value, the employee instances are ordered so that the int values ordered from 1 to 8.


EmpId Name Age
1 Jorge 19
2 Mark 30
3 Michel 10
4 Clerk 16
5 Frank 28
6 Bill 34
7 Simp 8
8 Lee 40
 

Sorting by other fields

If we need to sort using other fields of the employee, we’ll have to change the Employee class’s compareTo() method to use those fields. But then we’ll loose this empId based sorting mechanism. This is not a good alternative if we need to sort using different fields at different occasions. But no need to worry; Comparator is there to save us.

By writing a class that implements the java.util.Comparator interface, you can sort Employees using any field as you wish even without touching the Employee class itself; Employee class does not need to implement java.lang.Comparable or java.util.Comparator interface.

Sorting by name field

Following EmpSortByName class is used to sort Employee instances according to the name field. In this class, inside the compare() method sorting mechanism is implemented. In compare() method we get two Employee instances and we have to return which object is greater.


public class EmpSortByName implements Comparator<Employee>{

public int compare(Employee o1, Employee o2) {
return o1.getName().compareTo(o2.getName());
}
}

Watch out: Here, String class’s compareTo() method is used in comparing the name fields (which are Strings). 

Now to test this sorting mechanism, you must use the Collections.sort(List, Comparator) method instead of Collections.sort(List) method. Now change the TestEmployeeSort class as follows. See how the EmpSortByName comparator is used inside sort method.


import java.util.*;

public class TestEmployeeSort {

public static void main(String[] args) {

List coll = Util.getEmployees();
//Collections.sort(coll);
//use Comparator implementation
Collections.sort(coll, new EmpSortByName());
printList(coll);
}

private static void printList(List<Employee> list) {
System.out.println("EmpId\tName\tAge");
for (Employee e: list) {
System.out.println(e.getEmpId() + "\t" + e.getName() + "\t" + e.getAge());
}
}
}

Now the result would be as follows. Check whether the employees are sorted correctly by the name String field. You’ll see that these are sorted alphabetically.


EmpId Name Age
6 Bill 34
4 Clerk 16
5 Frank 28
1 Jorge 19
8 Lee 40
2 Mark 30
3 Michel 10
7 Simp 8
Sorting by empId field

Even the ordering by empId (previously done using Comparable) can be implemented using Comparator; following class 
does that. 


public class EmpSortByEmpId implements Comparator<Employee>{

public int compare(Employee o1, Employee o2) {
return o1.getEmpId() - o2.getEmpId();
}
}
 

