# MVC: Model View Controller



**Model–view–controller (MVC)** is a software architectural pattern. It divides an application into three interconnected parts. This allows you to separate internal representations of information from the ways that information is presented to (or accepted from) the user. This architecture has become extremely popular for designing web applications.

![](https://upload.wikimedia.org/wikipedia/commons/a/a0/MVC-Process.svg)

####Components
VC, the model, captures the behavior of the application in terms of its problem domain, independent of the user interface.[11] The model directly manages the data, logic and rules of the application.

A view can be any output representation of information, such as a chart or a diagram. Multiple views of the same information are possible, such as a bar chart for management and a tabular view for accountants.

The third part, the controller, accepts input and converts it to commands for the model or view.[12]

Interactions[edit]
In addition to dividing the application into three kinds of components, the model–view–controller design defines the interactions between them.[13]

A controller can send commands to the model to update the model's state (e.g. editing a document). It can also send commands to its associated view to change the view's presentation of the model (e.g. by scrolling through a document).
A model stores data that is retrieved according to commands from the controller and displayed in the view.
A view generates an output presentation to the user based on changes in the model.
A view controller generates an output view and an embedded controller