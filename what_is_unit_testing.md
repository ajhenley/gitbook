# What is unit testing?

As a developer you want to make sure your code works correctly, right? And so you create some tests for yourself. Those tests will not become part of the distributed application. They will not be used by the testers in your group. They have their own testing software to work with. Unit testing is how you, the developer, knows you code works witout having to go through a lot of effort each time to check and see.

###Why don't developers make good testers?
Things that seem simple to you are not always simple to your end user. When you test your code and it works that only indicates that the code your wrote as you understood the requirements works. What if you misunderstood the requirements? Or didn't read them correctly? Or didn't read them at all? Your test would pass but not to the client.

Testers should be testing the client's requirements. Developers can only test their own interpretations. "Hey, it works on my end!" is not an acceptable response to a client who can't log into the website you just created.

Unit testing is tests written by the developer to ensure the developer has created the code he intended. Now, when should you unit test? Just like voting in Chicago: early and often.

###What should you test? 
Everything. Your unit test is complete when every method in your application is included in a unit test. Some methods like private methods will be included indirectly. 

Unit testing helps you discover bugs before they become bugs. The act of thinking through how to test your code will uncover silly and stupid programming errors.
Unit testing forces you to think about those edge cases. 

###Unit tests as documentation
Unit tests are the best documentation you could write. A unit test describes how code should work. Unit tests can't get out of date. If you change your code you must change your unit tests or they will fail. Keeps you current, right?


###Unit tests make you a better, faster developer
If you design your application to be testable then you'll design a better application. You won't cram every line of code into main(). Instead you'll create testable classes. Better yet, if you 


Unit testing encourages better design. Knowing you need to write a unit test will force design considerations that otherwise take years of experience to realize. This can be a double-edge sword though, as I've seen bad design lead to worse design when unit tests are forced onto terrible existing code (i.e.: "I'll just make this thing public so I can access it from my test.")
Most importantly, unit testing provides a very important safety net for you. If you want to add a feature, refactor some code or hand your app off to another maintainer, there's a very clear signal if something breaks and the broken unit test will tell you where it's broken and how it's supposed to work.
The trick to unit testing is finding a good balance. If you're building a one-off app that you'll never touch once published, you can probably get away with little to no unit tests (it may not be worth it). Just know that going back and adding unit tests after the fact is not nearly as useful as writing it when you write the code you're testing (before or immediately after). If you're building a product that you plan to grow and maintain, unit testing will be invaluable, even if the app is simple. Just don't over-do it. Writing too many unit tests can be crippling in that the smallest change can require fixing hundreds of unit tests (EDIT: see further thoughts on this in the replies below). In general don't shoot for more than 70% line or branch coverage or you're probably overdoing it.