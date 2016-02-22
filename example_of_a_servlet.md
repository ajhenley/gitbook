<!--djw:done-->
###Example of a Servlet
You will be creating each servlet as a Java class in a Dynamic Web Application in Eclipse. Here is an example of the code for a simple servlet. It simply prints Hello, World! to the browser.


```java
package servlet;

import java.io.IOException;
import java.io.PrintWriter;

import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;

/**
 * Servlet implementation class Hello
 */
@WebServlet("/Hello")
public class Hello extends HttpServlet {

    private static final long serialVersionUID = 1L;

    /**
     * @see HttpServlet#HttpServlet()
     */
    public Hello() {
        super();
        // TODO Auto-generated constructor stub
    }

    /**
     * @see HttpServlet#doGet(HttpServletRequest request, HttpServletResponse response)
     */
    protected void doGet(HttpServletRequest request, HttpServletResponse response)              
                                               throws ServletException, IOException {
 
        // TODO Auto-generated method stub
       
        response.setContentType("text/html;charset=UTF-8");
        PrintWriter out = response.getWriter();
        try {
            out.println("Hello, World!");
        } finally {
            out.close();
        }
    }

    /**
     * @see HttpServlet#doPost(HttpServletRequest request, HttpServletResponse response)
     */
    protected void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
        // TODO Auto-generated method stub

        doGet(request,response);
    }
}
```


####Description
We notice two methods in this class: <code>doGet()</code> and <code>doPost()</code>. The first one anwsers by HTTP to the reception of a GET request, the second to the reception of a POST request. As we want that in the both cases the servlet processes the request, <code>doPost()</code> forwards to <code>doGet()</code>.

####Call the servlet from the browser
http://localhost:999/webTest/Greeting

####Result in the browser:
<pre>
Hello, World!
</pre>

####Mapping the Servlet to the URL
With Tomcat v. 7.0 and later you can use the @WebServlet annotation to map a servlet to a URL pattern. Simply code the URL pattern in parenthesis following the annotation, ```@WebServlet("/Hello")```.

####Decomposition of the URL
Calling the servlet's URL from the browser will request the servlet. You can also call the servlet from a link or formon a web page.
The URL is composed of the following parts:
Protocol: http or https
Domain: somedomain.com
Port (optional): the port which the servlet listens to
Root Entry Directory: the directory in which the servlet class file resides
Servlet Name: from the annotation mapping
[Protocol://][Domain]:[PORT]/[RootEntryDirectory]/[ServletName]
