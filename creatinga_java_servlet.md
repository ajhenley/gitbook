###Creating a Java Servlet
Create a new Dynamic Web Project in Eclipse. You are going to create a java servlet!

Servlets are Java classes which service HTTP requests and implement thejavax.servlet.Servlet interface. Web application developers typically write servlets that extend javax.servlet.http.HttpServlet, an abstract class that implements the Servlet interface and is specially designed to handle HTTP requests.

Sample Code for Hello World:

Following is the sample source code structure of a servlet example to write Hello World:

{%ace edit=true, lang='java'%}
// Import required java libraries
import java.io.*;
import javax.servlet.*;
import javax.servlet.http.*;

// Extend HttpServlet class
public class HelloWorld extends HttpServlet {
 
  private String message;

  public void init() throws ServletException
  {
      // Do required initialization
      message = "Hello World";
  }

  public void doGet(HttpServletRequest request,
                    HttpServletResponse response)
            throws ServletException, IOException
  {
      // Set response content type
      response.setContentType("text/html");

      // Actual logic goes here.
      PrintWriter out = response.getWriter();
      out.println("&lt;h1&gt;" + message + "&lt;/h1&gt;"); 
   } 

   public void destroy() 
   { 
     // do nothing. 
   } 
}
{%endace%}

What you should do now

View Source on the resulting web page. What is missing? Can you figure out how to add the missing pieces of web page? Do so
Make the title (the text on the browser tab) set by a variable called titleString