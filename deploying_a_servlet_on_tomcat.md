###Deploying a Servlet 

The servlet name will be determined by the annotation at the top of the servlet code file. In this case the servlet is called hello.

```java
@WebServlet(value="/Greeting")
public class GreetingServlet extends HttpServlet {

    @Override
    public void doGet(HttpServletRequest request,HttpServletResponse response)
        throws ServletException, IOException {
    PrintWriter out = response.getWriter();

    // then write the data of the response
        out.println("<h2>Hello, World!</h2>");
    }

}
```

####Call of the servlet from the browser
http://localhost:999/webTest/Greeting

####Result in the browser:

<h2>Hello, World!</h2>


####Decomposition of the URL
[Protocol://][Domain]:[PORT]/[RootEntryDirectory]/[ServletName]

