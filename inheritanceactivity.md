# Inheritance activity

Using the code from the Inheritance Completion Activity, create a toString method on the superclass and the subclasses such that all the relevant information about an object is returned if you use thisObject.toString().

After you create the method and the two overrides, wrap the classes in application that allows the user to input any number of either books or a pieces of software (user's choice) and then outputs the information about all the inputs (toString()) in a list after the user is done.

BONUS: Just to keep things interesting, the toString method on the superclass should take no parameters, while the toString method on the subclasses should take a detail parameter (String). If detail is set to "simple", the method should return the same thing that the superclass method would return, while if it is set to "detail" then the method should return all the attributes included in the subclass.