###Example of a Servlet

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
            out.println("Hello World");
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

####Call of the servlet from the browser
http://localhost:999/webTest/Greeting

####Result in the browser:

<h2>Hello, World!</h2>


####Decomposition of the URL
[Protocol://][Domain]:[PORT]/[RootEntryDirectory]/[ServletName]
