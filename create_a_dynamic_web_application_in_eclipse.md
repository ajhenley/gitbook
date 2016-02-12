###Create a Dynamic Web Application in Eclipse
File | New | Dynamic Web Project
Type in a project name
select Apache Tomcat v. 7.0 for the target runtime
Click Next twice and then click Finish

Your servlet code files will  be placed under Java Resources | src folder. You can create subfolders under that.
Your html and jsp code will be placed under the WebContent folder. Again, you can create subfolders as necessary. For example, you'll probably have subfolders for images, javascript and 

Lastly, you'll need to add the jar files to the WebContent/WEB-INF/lib folder. And add them to the build path. Simply find the ojdbc6.jar file on your computer and copy it to this folder.



Right-click on the project name and select Build Path | Configure Build Path
The Properties window will open and you should select the Libraries tab if it isn't selected already.
Click the button to Add External JARs. Browse for the ojdbc6.jar file. You can browse to the .jar you placed in WEB-INF/lib or the one on your computer. Do not select a jar file on the network. Eclipse has trouble finding those.

####Create your first web page

####Create your first servlet


####Test it out

####Your Assignment
Create a new dynamic web application with a web page and a servlet. It should display your name.


