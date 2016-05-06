<!--djw:done-->
###Expression Language (EL) 

The Expression Language (EL) is a faster/easier way to display parameter values. It is part of the JSP Specification. Expression Language is helpful for web designers. They may have limited Java knowledge yet still have the need to send and receive data from servlets or other Java objects. EL does this by encoding tags in the JSP. It is possible to use scriptlet tags ```<%``` and``` %>``` to accomplish the same task but EL simplifies this process.

```html
Hello, ${param.visitor}
```
Same as
```html
Hello, <%=request.getParameter("visitor")%>
```
EL offers a clearer way to navigate nested beans. Consider some beans:

{%ace edit=false, lang='java'%}
class Person {
   String name;
   // Person nests an organization bean.
   Organization organization;

   public String getName() { return this.name; }
   public Organization getOrganization() { return this.organization; }
}
{%endace%}

{%ace edit=false, lang='java'%}
class Organization {
   String name;
   public String getName() { return this.name; }
}
{%endace%}

If an instance of Person was to be placed onto a request attribute under the name "person", the JSP would have:
{%ace edit=false, lang='html'%}
 Hello, ${person.name}, of company ${person.organization.name}
{%endace%}

Same as.

{%ace edit=false, lang='html'%}
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
{%endace%}
