###Create abstract vehicle class
Modify your Car Class application. Now you will need to create an abstract class for a Vehicle. The Vehicle can run and stop and accelerate like all vehicles can. However the abstract class can not fly like a plane or float like a boat. Nor can it haul 40 tons of book objects like a semi-trailer. For those specific implementations you'll need to inherit your abstract class using the keyword extends. Then you can create a Plane class, a Boat class and a Car class all of which inherit from the Vehicle class.

 

You can make your Plane, Boat and Car implementations final by using the keyword final after the modifier public in the class definition to prevent your class from being inherited by someone else. This isn't common but you may sometimes see people do this. Also, you can prevent a specific method from being overridden in the same way.

Note: If a constructor does not explicitly invoke a superclass constructor, the Java compiler automatically inserts a call to the no-argument constructor of the superclass. If the super class does not have a no-argument constructor, you will get a compile-time error. Object does have such a constructor, so if Object is the only superclass, there is no problem.

 