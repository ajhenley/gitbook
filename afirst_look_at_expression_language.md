# A first look at Expression Language

Create a new dynamic web application that contains a class for a user. You do not have to connect to the database for this example. Simply create a user class and a servlet.

Once you create a user and populate the name and some other values then put that user object in the session.

How to add the user to the session:
```java
User user = new User(firstName, lastName, email);
session.setAttribute("user", user);
```
 

Create a JSP page.

Display the user on the JSP page using the following code:

 
```java
 Hello ${sessionScope.user.firstName}
```
Also display the other fields in your class.

The above code fragment is called Expression Language. It can be used in JSP pages to display objects stored in the session.

Now create another JSP page.

Create a link in the first JSP page to the new JSP page.

Copy the code above. Will it work?

What happens if you remove sessionScope from the attribute?

 

Next, create an object called Address.java. An address contains the following attributes: Street Address, City, State, ZIP.

Add the Address class to the User object.

Note: The Address class must be a class in the User class. So, a User HAS An Address.

Modify your JSP page to display the User's Address.

