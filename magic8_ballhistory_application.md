###Magic 8 ball history application
You can extend a class even if that class that isn't Abstract. Why would you do that?

Remember, it's better to extend than to rewrite. Tested, functional code should be left alone to continue doing what it's been doing. If you find you need additional functionality then simply extend the class to add that functionality.

So if you have a functional Fortune class that properly asks questions and you want to add history to it (to remember all the questions and answers) then you don't change the 8 ball. You simply extend Fortune into a new class called FortuneRemembers. 

Your mission is to extend your Magic 8 ball class. Start by creating a new class called FortuneRemembers. The new class will inherit all the methods from the Fortune class (which does not have to be an abstract class to be inherited). You'll still use the extends keyword in your Fortune class.

Take the code from the previous exercise and extend the application to allow the user to "Ask" a question of the system. The random answers are displayed to the user asking the questions. Now the system should remember all the questions and the answers. And if the user enters "history" as their question, then instead of generating an answer, the system should output all the questions and answers generated so far.

This application should use multiple classes and methods. Don't put everything in the main() method. That makes the kittens on YouTube sad.
