<!-- this is the tutorial slowly I turned -->
There are a number of steps to create a JPA project. Follow along with this walkthorugh and pretty soon you'll have a good idea how to create a JPA project. Due to differences in Eclipse versions, your screens may differ slightly. You can create a JPA project for a Java project or for a Dynamic Web Project.

1) First Create a New Java Project….

![](images/slowlyiturned/image10.png)<br>

2) Click the Next button (not the Finish button) and get to the Java Settings screen.

![](images/slowlyiturned/image12.png)<br>

3) Click on the Libraries tab so you can add the necessary jar files to the build path. You will need to add 3 jar files: EclipseLink, JavaPersistence and OJDBC.<br>
![](images/slowlyiturned/image11.png)<br>
4) Click on the Add External JARs… button and select the eclipselink.jar file and click Open. <br>
![](images/slowlyiturned/image14.png)<br>
5) Click on the Add External JARs… button and select javax.persistence_2.1.0.v201304241213.jar (or whatever the current version is)<br>

![](images/slowlyiturned/image13.png)<br>

6) Click on the Add External JARs… button and select ojdbc6.jar (or whatever the current version is) and click Finish.<br>

![](images/slowlyiturned/image16.png)<br>
7) Right-Click your project in the Project Explorer and select Properties from the drop-down.<br>
![](images/slowlyiturned/image15.png)<br>
8) Select Project Facets from the list on the Left…<br>

![](images/slowlyiturned/image20.png)<br>
9) If you see the screen below, you need to click the “Convert to faceted form…” link…<br>
![](images/slowlyiturned/image18.png)<br>
10) This project has a Java version level that is too low.  The Java version should be 1.7 or higher.<br>
Make the window a little wider so that you can see the controls to increase the Java level.<br>

![](images/slowlyiturned/image25.png)<br>
11) Click the drop-down triangle next to the number that is on the line with the Java Project Facet.<br>
![](images/slowlyiturned/image21.png)<br>
12) Click on the checkbox next to JPA and you will be asked to do some configuration. Click the link and get the following screen. Set the following:<br>
Platform: to EclipseLink<br>
JPA Implementation Type: Disable Library Configuration<br>
Connection: to the name of your connection. <br>
Once this is done click the connect link immediately under and to the right of the connection drop down. 
And then click OK.<br>

![](images/slowlyiturned/image23.png)<br>
13) Click Apply to save your JPA settings…<br>

![](images/slowlyiturned/image26.png)<br>

14) Look in the JPA Content container inside your project and double-click the persistence.xml file.<br>

![](images/slowlyiturned/image28.png)<br>
15) This is the dialog box for configuring your persistence.xml file<br>
![](images/slowlyiturned/image29.png)<br>
16) If you click the General tab, you will see the raw xml of the persistence file. It doesn’t look like much yet but as we set our configuration more tags will be added.<br>
![](images/slowlyiturned/image30.png)<br>
17) On the General tab, set the Persistence Provider to  org.eclipse.persistence.jpa.PersistenceProvider
![](images/slowlyiturned/image31.png)<br>
18) Uncheck the Exclude unlisted classes checkbox…<br>

![](images/slowlyiturned/image32.png)<br>
19) On the connection tab, change the Transacation Type to Resource Local…<br>
![](images/slowlyiturned/image33.png)<br>
20) After that, click the Populate from connection link…<br>

![](images/slowlyiturned/image34.png)<br>
21) A dialog will appear asking you to select your connection, click Ok after you have done so…<br>
![](images/slowlyiturned/image00.png)<br>
22) The dialog should now look like this… Note: the URL may be slightly different depending on your system. It’s also possible you have a different value for User.<br>

![](images/slowlyiturned/image01.png)<br>

23) If you click on the source tab, the XML should now look approximately like this… <br>
Save the file changes (click the icon in Eclipse to save) and you are done…<br>
![](images/slowlyiturned/image02.png)<br>
24) Right-Click your project and Select New… JPA Entities from Tables…<br>

![](images/slowlyiturned/image03.png)<br>
25) This is the Generate Custom Entities dialog. If you completed all the previous steps you should see your connection listed. When connected you will see your schemas and tables listed…<br>
![](images/slowlyiturned/image04.png)<br>
26) Once you have selected the Connection, the Schema and at least one Table, you should see the Next button activate.<br>

![](images/slowlyiturned/image05.png)<br>
27) This screen will be blank if you have only selected one table (and possibly even if you have selected multiple tables but they don’t have any relationship to each other)<br>
![](images/slowlyiturned/image06.png)<br>
28) Hit Next on this screen too…<br>

![](images/slowlyiturned/image07.png)<br>
29) Hit Next again (but this is where you would customize the name of the class and/or the names of the columns)…<br>
![](images/slowlyiturned/image08.png)<br>
30) Once you click Finish, you should right-click the project name again…<br>
![](images/slowlyiturned/image09.png)<br>
31) Select New… Class…<br>
![](images/slowlyiturned/image17.png)<br>
32) This is the class creation dialog, the main things you want to do are set your Package to customTools, your name to DBUtil and then click Finish…<br>

![](images/slowlyiturned/image19.png)<br>
33) Eclipse will open your DBUtil.java class ready for editing. Edit it to look something like this…<br>
Replace name of your persistence unit with the name of your persistence unit.<br>

```java
package customTools;

import javax.persistence.EntityManager;
import javax.persistence.EntityManagerFactory;
import javax.persistence.Persistence;

public class DBUtil {
private static final EntityManagerFactory emf = 
Persistence.createEntityManagerFactory("name of your persistence unit");
	public static EntityManagerFactory getEmFactory() {
		return emf;
	}
}
```
34) Right-Click the Project Name and Select New… Class…<br>

![](images/slowlyiturned/image22.png)<br>
35) For this class just pick a name and check the public static void main(String[] args) checkbox…<br>

![](images/slowlyiturned/image24.png)<br>
36) After you click Finish, edit the class to look like this:<br>

```java
import javax.persistence.EntityManager;
import data.DBUtil;

public class QS3 {
	public static void main(String[] args) {
		EntityManager em = DBUtil.getEmFactory().createEntityManager();
		try {
			model.DemoCustomer cust = em.find(model.DemoCustomer.class, (long)2);
			System.out.println(cust.getCustFirstName());
		} catch (Exception e){
			System.out.println(e);
		} finally {
			em.close();
			System.out.println("cerrado!");
		}
	}
}

```
37)  Edit the Generated Class and add ```schema=”TESTUSER”``` to the table annotation like you see on line 13.<br>

![](images/slowlyiturned/image27.png)<br>

38) Now you are done…Run it and you should see the Customer name (and no errors).<br>
If it didn’t work then most likely you’ve skipped a step or have a typo. Go through the tutorial again - this time reviewing your work.

