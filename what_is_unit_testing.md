# What is unit testing?

Unit testing is used by you - the developer. The unit tests are not part of the distributed application. They are not for use by the testers in your group. Let them write their own tests. They shouldn't be getting their instructions from the developers anyway. The testers should be testing the client's requirements not the developer's interpretations.

When should you unit test? Just like voting in Chicago: early and often.

What should you test? Everything. Your unit test is complete when every method in your application is included in a unit test. Some methods like private methods will be included indirectly. 