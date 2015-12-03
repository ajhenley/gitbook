# What is integration testing?

Unit tests allow you to validate your application business logic. Unit tests do not ensure the deployability of your amazing shiny new Java application.For that we turn to integration testing.

###Integration Testing
* Example: getting data out of the data database and sending an email to the logged in user
* verifies implementation of individual components and their interconnected behavior
* tests the system
* depends on the environment
* could fail even if your code works perfectly. Some reasons might include:
    * incorrect configuration information for database or mail server
    * network problems
* 

###Unit Testing
* Example: testing that your method to getAge() for a user returns the correct age