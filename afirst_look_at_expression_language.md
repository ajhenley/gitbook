<!--djw:done-->
Create a new dynamic web application that contains a class for a user. You do not have to connect to the database for this example. Simply create a user class and a servlet.

Once you create a user and populate the name and some other values then put that user object in the session.

####How to add the user to the session:
{%ace edit=false, lang='java'%}
User user = new User(firstName, lastName, email);
session.setAttribute("user", user);
{%endace%}
 
Create a JSP page. When the above code executes it will populate the user class and add it to the session. You can display the user on the JSP page using the following code:

{%ace edit=false, lang='java'%}
Hello ${sessionScope.user.firstName}
{%endace%}

The above code fragment is and example of Expression Language. It's a shortcut notation your JSP pages can use to display objects stored in the session. The word ```sessionScope``` is optional. The woud ```user``` is the name of the attribute from the servlet. It contains an instance of a User object which is in the session. The word firstName is formed by removing the word get from the getter, getFirstName(), and changing the case of the starting letter. It is also the same as the private variable in the User class but it actually comes from the getter.

<div style="page-break-after: always;"></div>
####Your first Java Bean
The User class in this example is a Java Bean. It's a class that meets the following criteria: all instance varibles are private and they are available through public getters and setters. It also must serializable. 


####Here's the code for the User class:
{%ace edit=false, lang='java'%}
public class PersonBean implements java.io.Serializable {
    private String name = null;
    public String getName(){
        return name;
    }
    public String setName(String value){
        name = value;
    }
{%endace%}

####Your Assignment
1. Create another JSP page.
2. Create a link in the first JSP page to the new JSP page.
3. Copy the code above. Will it work?
4. Display the other fields in your class.
5. What happens if you remove sessionScope from the attribute?
 
####Your second Assignment
1. Next, create an object called Address.java. An address contains the following attributes: Street Address, City, State, ZIP.
2. Add the Address class to the User object. The Address class must be a class in the User class. A User HAS An Address.
3. Change your JSP page to display the User's Address.

