The Expression Language (EL) is a faster/easier way to display parameter values. It is available since JSP 2.0 . For instance, it allows developers to create Velocity-style templates:
```html
Hello, ${param.visitor}
```
Same as
```html
Hello, <%=request.getParameter("visitor")%>
```
It also offers a clearer way to navigate nested beans. Consider some beans:

```java
class Person {
   String name;
   // Person nests an organization bean.
   Organization organization;

   public String getName() { return this.name; }
   public Organization getOrganization() { return this.organization; }
}
```

```java
class Organization {
   String name;
   public String getName() { return this.name; }
}
```

Then, if an instance of Person was to be placed onto a request attribute under the name "person", the JSP would have:
```html
 Hello, ${person.name}, of company ${person.organization.name}
```

Same as.

```html
 Hello,
<% Person p = (Person) request.getAttribute("person");
   if (p != null) {
       out.print(p.getName());
   }
%>, of company
<% if ((p != null) && (p.getOrganization() != null)) {
       out.print(p.getOrganization().getName());
   }
%>
```
