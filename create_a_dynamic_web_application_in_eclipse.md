###Create a Dynamic Web Application in Eclipse
Congratulations for making it this far. You've learned a lot! You know how to create object-oriented Java applications and even some HTML. Now you're going to combine that knowledge to develop a true enterprise application.

####What is an enterprise application? 
Software developed for business that lots of people depend on is an enterprise application. It's unlikely in business that you'll create a lot of desktop applications. That's why this course is focusing on developing enterprise applications. Businesses want software that is scalable, distributed and mission-critical. Most of all they want software to work. All the time. That's why we'll focus on not only developing software but also testing it.

Web applications can meet these requirements. When you think of enterprise software think websites. The format solves a lot of problems for which desktop software is unsuitable. Websites have one code-base on the server. When it's updated then every user is also updated. Users with different versions are a thing of the past.

####How to create a dynamic web project in Eclipse. 
1. From the Eclipse menu, select on File | New | Dynamic Web Project
2. On the window that pops up, type in a project name
3. Select 'Apache Tomcat v. 7.0' for the target runtime
4. Click Next twice. Then click Finish.
5. You'll need to add the jar files to the ```WebContent/WEB-INF/lib folder```. Browse your computer to find the ojdbc6.jar file on your computer and copy it to this folder.
6. Right-click on the project name and select Build Path | Configure Build Path
The Properties window will open and you should select the Libraries tab. Click the button to Add External JARs. Browse for the ojdbc6.jar file. You can browse to the .jar you placed in WEB-INF/lib or the one on your computer. Do not select a jar file on the network. Eclipse has trouble finding those.

* Your servlet code files will  be placed under Java Resources | src folder. You can create subfolders under that if you like.
* Your html and jsp code will be placed under the WebContent folder. Again, you can create subfolders as necessary. For example, you'll probably have subfolders for images and javascript.

Next, you'll create a servlet that sends it's output to a web page.

####The components of the dynamic web project
* JavaServer Pages (JSP) - web pages that integrate Java code with HTML or XML. You can use JSP technology to create dynamically generated web pages. 
* Servlets - a small Java program that runs within a web server. The servlet actually extends the webserver giving it the abiltiy to return a customized response to a request. The Java servlets in this course will generally send their output to the JSP.

####Create your first JavaServer Page (JSP)


####Create your first servlet


####Test it out

####Your Assignment
Create a new dynamic web application with a web page and a servlet. It should display your name.


