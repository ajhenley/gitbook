<!--djw:done for now
djw 03.10.16 massive rewrite
-->
###Encapsulation
Sometimes your class has some internal business to attend to.

For example, your class may contains a method called save which takes as its argument the filename.

The class exposes (makes available) the save method.

Once the user of your class calls the save method your class still has work to do. It must determine if the file exists. If the file doesn't exist then your class must create it on the disk. Then write the data. Finally, close the connection to the file.

Encapsulation ensures that the user only knows about the save method and not every little detail required to make the save method work.

Public, Private and Protected, oh my!

Getters/setters only allow private member variables to expose their data IF you want them to expose their data. A variable not exposed via a getter or setter is effectively hidden (unless it's declared public which isn't recommended). It may be used only by the class. If you want that variable to be visible only to your class then declare it as private. If you want it to be visible only to the class and any future subclasses then declare it as protected. In any event the user has no idea it exists. It's secret to my class (and possibly subclasses).

A variable can have an access modifier
Public - visible to any class in your program
Private - visible only to your class (not sub classes)
Protected - visible to your class and any subclasses (also visible to any classes in the same package)

You could also have a variable that has only a getter. That would be a read-only variable. or you could have a variable with only a setter. That would be a write-only variable (not common though).

You could also have private variables like counters and things that only you class uses and nobody else uses. Since there would be no getters/setters for those variables they would be private to the class. Unless you declared them as protected. Then they would be visible to the class and subclasses. But the class/subclass may use them for all kinds of things like database login information or something. Or saving files.

So how would the value of a private member variable with no getters or setters get set? If it was database connection information then maybe in the constructor the class could read from a settings file that contained the database settings. This file might be encrypteed so it's useless to everyone. But our class may have the decrypt method build in and will read the settings in the constructor can connect to the database.

A lot of the databases connection code is encapsulated in JPA so you only have to set a few things in the settings file and the JPA classes know how to connect to oracle or whatever database you're using.

