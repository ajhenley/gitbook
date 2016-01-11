<!--djw:done for now-->
###Encapsulation
Sometimes your class has some internal business to attend to. Maybe your class contains a method called save which takes as its argument the filename. The interface exposes (makes available) the save method but once the user of your class calls that method your class still has to make sure the file doesn't exist create it on the disk, write the data and close the connection to the file. Encapsulation ensures that the user only knows about the save method and not every little detail required to make save work.



