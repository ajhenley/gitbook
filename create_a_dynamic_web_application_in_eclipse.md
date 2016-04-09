<!--djw:done-->
###Create a Dynamic Web Application in Eclipse
Congratulations for making it this far. You've learned a lot! You know how to create object-oriented Java applications and some HTML. You can use that knowledge to develop a true enterprise application.

####What is an enterprise application? 
Software developed for business that lots of people depend on is an enterprise application. It's unlikely in business that you'll create a lot of desktop applications. That's why this course focuses on web applications. Businesses want software that is scalable, distributed and reliable. We meet those goals by focusing developing software and testing it.

####How to create a dynamic web project in Eclipse. 
1. From the Eclipse menu, select File | New | Dynamic Web Project
2. On the window that pops up, type in a project name
3. Select 'Apache Tomcat v. 7.0' for the target runtime
4. Click Next twice. Then click Finish.
5. You'll need to add the jar files to the ```WebContent/WEB-INF/lib folder```. Browse your computer to find the ojdbc6.jar file on your computer and copy it to this folder.
6. Right-click on the project name and select Build Path | Configure Build Path
The Properties window will open and you should select the Libraries tab. Click the button to Add External JARs. Browse for the ojdbc6.jar file. You can browse to the .jar you placed in WEB-INF/lib or the one on your computer. Do not select a jar file on the network. Eclipse has trouble finding those.

* Your servlet code will  be placed under Java Resources | src folder. You can create subfolders under that if you like.
* Your html and jsp code will be placed under the WebContent folder. Again, you can create subfolders as necessary. For example, you'll probably have subfolders for images and javascript.

Next, you'll create a servlet that sends it's output to a web page.

####The components of the dynamic web project
* JavaServer Pages (JSP) - web pages that integrate Java code with HTML or XML. You can use JSP technology to create dynamically generated web pages. 
* Servlets - a small Java program that runs within a web server. The servlet actually extends the web server so it can return a customized response to a request. The Java servlets in this course will generally send their output to the JSP.

####Create an index.html page
The entry point for many websites is index.html. That is the page the user first sees upon visiting your site and will be the page that sends the user to other pages within the site.

{%ace edit=true, lang='html'%}
<!-- index.html goes in the /WebContent folder -->
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Greeting Servlet Web Page</title>
</head>
<body>
<form action="greetingServlet" method="post">
<label>Enter Your Name:</label>
<input type="text" name="firstName" value="" size="15">
<input type="submit" id="submit" value="Greet me!">
</form>
</body>
</html>
{%endace%}
<div style="page-break-after: always;"></div>
####Create your first servlet
The ```action``` attribute of index.html tells the web server to direct the form's output to the ```greetingServlet```. The servlet will process the form data from index.html and return it to the output.jsp page.

The form data is submitted using the post method so the ```doPost()``` method responds. In this method the servlet retrieves the posted data. Next, the servlet sets the name attribute and redirects the response to the jsp page.

{%ace edit=true, lang='java'%}
//FormProcessor.java goes in the /scr folder
import java.io.IOException;
import javax.servlet.ServletException;
import javax.servlet.annotation.WebServlet;
import javax.servlet.http.HttpServlet;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;

@WebServlet("/greetingServlet")
public class FormProcessor extends HttpServlet {
	private static final long serialVersionUID = 1L;
       
    public FormProcessor() {
        super();
    }

	protected void doGet(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
		doPost(request,response);
	}

	protected void doPost(HttpServletRequest request, HttpServletResponse response) throws ServletException, IOException {
		//get the parameter 
		String name = request.getParameter("firstName");
		String url = "/greeting.jsp";
		if (name == null || name.length()==0) {
			name = "Unnamed Person";
		}
		request.setAttribute("name",name);
		getServletContext().getRequestDispatcher(url).forward(request, response);
	}

}
{%endace%}
<div style="page-break-after: always;"></div>
####Create your first JavaServer Page (JSP)
The JSP will accept the attribute from the servlet and set its value to the name.

{%ace edit=true, lang='java'%}
<!--  greeting.jsp goes in the /WebContent folder -->
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<title>Greeting Servlet</title>
</head>
<body>
<h1>Welcome,${name}</h1>
</body>
</html>
{%endace%}

####Your Assignment
Create a new dynamic web application with a web page and a servlet. It should display your name. Copy the code above to the file locations indicated by the comment on the first line.
Run your project. Since you want to start with the index.html page you should select index.html from the project explorer in Eclipse. Right-click on this file. Select Run As | Run on Server from the pop-up menu.

####Improve your application
Modify your JSP page to include Bootstrap.






