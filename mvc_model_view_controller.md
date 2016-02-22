<!--djw:done-->
###MVC: Model View Controller

**Model–view–controller (MVC)** is a software architectural pattern. It divides an application into three interconnected parts. This allows you to separate internal representations of information from the ways that information is presented to (or accepted from) the user. This architecture has become extremely popular for designing web applications.

![](https://upload.wikimedia.org/wikipedia/commons/a/a0/MVC-Process.svg)

####Components
**The model** directly manages the data, logic and rules of the application.

**A view** can be any output representation of information, such as a chart or a diagram. Multiple views of the same information are possible, such as a bar chart for management and a tabular view for accountants. In applications you will create the view will be the web page.

**The controller** accepts input and converts it to commands for the model or view. The controller can also manage the logic and rules of the application. 

####Interactions between the components
* A controller can send commands to the model to update the model's state (e.g. editing a document). It can also send commands to its associated view to change the view's presentation of the model (e.g. by scrolling through a document).
* A model stores data that is retrieved according to commands from the controller and displayed in the view.
* A view generates an output presentation to the user based on changes in the model.


####How this affects you
When you develop an application you'll create a database. The model will represent the database. Secondly you'll develop a page for the user. This is the view, also called the presentation. Finally, you'll code some business rules that the client wants the application to enforce. These go into the controller along with code help the view interact with the model.