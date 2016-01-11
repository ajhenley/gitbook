<!--djw:done-->
###Create a car class and app

Create a project in Eclipse called CarApplication

Create a class called Car. The Car class shall contain the following:
* private member variables
* a default constructor
* an overloaded constructor 
* methods which print each task the car is performing. 

For example, the accelerate method will return a string that says "The car is accelerating" and the setSpeed(90) method will return a string that says "The Speed is 90 mph". 
The application shall also contain getters and setters for each private member variable.

Create another class called CarApp which contains the main method. In the main method you shall create an instance of a Car and print the different methods as the car object is "operated". Your output should look something like this:

```
The red Porsche is starting
The blue Jetta is starting
The red Porsche is accelerating
The blue Jetta is accelerating
The blue Jetta has stopped to have it's emissions checked 
The blue Jetta passes it's emission test
The red Porsche is going 50 mph
The red Porsche is stopped
The blue Jetta just passed the red Porsche
```
 
Be creative and make up your own methods if you like. 

Create a second instance of the car once your first car is working. Set it's private member variables in the main method. Now you can call the methods of the second car in between the calls to the methods of the first car. Your program will keep the two separate. Here's an example. Your mileage may vary.

```
The red Porsche is starting
The blue Jetta is starting
The red Porsche is accelerating
The blue Jetta is accelerating
The blue Jetta has stopped to have it's emissions checked 
The blue Jetta passes it's emission test
The red Porsche is going 50 mph
The red Porsche is stopped
The blue Jetta just passed the red Porsche
```