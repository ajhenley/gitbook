###Composition vs Inheritance Explained
Both composition and inheritance enable a class to reuse the code of another class. Programmers may use inheritance to get one class to contain the functionality of another. Sometimes that's the best idea in the world. Sometimes it's a square wheel. Which to use and when? The correct answer depends on the relationship between the classes.

With Composition you learned how a Person class could have a Job. Or an Education class could contain schools. We call these *has-a* relationships because the first class *has-an* object of the second class. 

Inheritance is the other type of relationship. It occurs when one class inherits another. An Employee class is a more specific instance of a Person. It inherits the Person class. This type of relationship is called an *is-a* relationship. All the attributes of Person are in Employee as well as some attributes specific to Employees. Such as Department, Manager, PayRate, etc... 


###What You Should Try Now
Create an Education class and make an instance of the Education class a member of the Person class. Your education class should include a list of last 10 schools attended.
Create a toString override for both Job and Education that outputs the information in the class to the console. The toString override for Person should use the toString methods for the Job and Education member objects.


