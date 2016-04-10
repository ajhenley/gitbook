<!--djw-->
<!--todo: need assignment for cookies-->
You can pass data between servlets and JSP pages with objects stored in the session. You can also use cookies.

####How to create and access a cookie
Servlet code
{%ace edit=false, lang='java'%}
Cookie c = new Cookie("emailCookie", email);
c.setMaxAge(60*60); //set its age to 1 hour
c.setPath("/"); //allow the entire application to access it
response.addCookie(c);
{%endace%}

JSP code
{%ace edit=false, lang='java'%}
<p>The email cookie: ${cookie.emailCookie.value}</p>
{%endace%}


