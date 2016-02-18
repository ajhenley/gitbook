###Deploying a Servlet on Tomcat

* Put the compiled class with its package in the directory <code>classes</code> in <code>WEB-INF</code> of the working web directory (here: <code>webTest</code>)
* Edit <code>web.xml</code> in <code>WEB-INF</code> by adding:

```java
<web-app xmlns="http://java.sun.com/xml/ns/javaee"
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://java.sun.com/xml/ns/javaee
                      http://java.sun.com/xml/ns/javaee/web-app_3_0.xsd"
  version="3.0"
  metadata-complete="true">  

  <!-- Beginning here -->

    <servlet>
      <servlet-name>Hello</servlet-name><!-- Class name -->
      <servlet-class>servlet.Hello</servlet-class><!-- Class tree: with the package -->
    </servlet>
    <servlet-mapping>
        <servlet-name>Hello</servlet-name><!-- Class name -->
        <url-pattern>/Hello</url-pattern><!-- Class pattern in the URL-->
    </servlet-mapping>

   <!-- End here -->

<web-app>
```java

So the <code>WEB-INF</code> contains:

<pre>
   WEB-INF
     web.xml
     classes
       servlet
         Hello.class
</pre>

####Call of the servlet from the browser
http://localhost:999/webTest/Hello

Result in the browser:
<pre>
Hello World
</pre>

####Decomposition of the URL
[Protocol://][Domain]:[PORT]/[RootEntryDirectory]/[ServletName]

