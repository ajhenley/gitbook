<!--djw:done-->
Now that we've talked about how we can make our code better and more organized by creating classes lets talk a little about how the classes fit together. 


Like every Java program, you completed program will contain a method called ```main```. This is the entry point to your program. You may have putting most of your code in the main method but not that stops. Now you'll put most of your code in classes and the main method will simply call the classes as they are needed. The classes may call other classes, etc.

Your program will be generally divided into three tiers. The usual three tiers are presentation, business layer and database (or file) layer. 

####What happens in each tier
**Presentation Layer** this is your user-interface. It's the console for a command-line program and the web pages for a web application.

**Business Layer** this contains your business rules. It's where you write the code that determines how your data will be created, displayed, validated or changed. Nothing gets to the database except through the business layer.  Your business's policies are enforced at this layer. If the presentation layer is your front door then the business layer is bouncer just inside.

**Database Layer** this contains the persistent storage for your validated data. It can be an actual database like Oracle or it can be the hard drive where files are saved in various formats.

