<p>For Java University we're creating a login page, a data entry page and a report page. The data entry page will allow us to enter a single record and when you click submit it will go to the report page.</p>
<p>Login Page will contain a form with an action called process.jsp. The method should be post. &nbsp;Normally we won't use jsp pages in this manner. We'll use servlets instead. They have more features for handling such requests. However, a JSP allows us to quickly pass the parameters to other pages without a servlet.</p>

```html
&lt;!DOCTYPE html&gt;<br />&lt;html&gt;<br />&lt;head&gt;<br />&lt;meta charset="ISO-8859-1"&gt;<br />&lt;title&gt;Insert title here&lt;/title&gt;<br />&lt;/head&gt;<br />&lt;body&gt;<br />&lt;form action="process.jsp" method="post"&gt;<br />&lt;input type="text" name="user"&gt;&lt;/input&gt;&lt;br/&gt;<br />&lt;input type="text" name="password"&gt;&lt;/input&gt;<br />&lt;input type="submit"&gt;&lt;/input&gt;<br />&lt;/form&gt;<br />&lt;/body&gt;<br />&lt;/html&gt;</pre>
<p>&nbsp;</p>
<p>The process.jsp page should look like this:</p>
```html
<%@ page language="java" contentType="text/html; charset=ISO-8859-1"<br /> pageEncoding="ISO-8859-1"%>
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=ISO-8859-1"><title>Insert title here </title></head>
<body>
Welcome, <%= request.getParameter("user")
Your password is <%=request.getParameter("password")%>
</body>
</html>
```


<p>Get the process page working then add a link to the data entry&nbsp;page. On&nbsp;the data entry page you will create a form with an action="report.jsp" and method="post". That will display the values from your one record. If we wanted to display lots of records we would need a database and a servlet so that comes later.</p>
<p>&nbsp;<strong>Bonus</strong>: Display the user's name and current date on the report page.</p>
