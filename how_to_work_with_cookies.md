<!--djw-->
<!--todo: need assignment for cookies-->
###Saving State with Cookies
You can pass data between servlets and JSP pages with objects stored in the session. You can also use cookies.

A cookie is a file a web site can store on the user's computer. The website can retrieve the data in the cookies when the user visits the site again. This allows the website to recognize the user. A cookie can save the user from re-entering information. The cookie can personalize the experience by "remembering" the user.

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


