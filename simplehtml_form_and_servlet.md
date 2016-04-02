<!--djw:done-->
###Create a Form Processing Servlet
You've successfully created an HTML form. It looks great. It does nothing. Now let's get the data from your form and into your servlet.
Read the page called *Get and Post Details* for additional information.

####Your assignment
1. For the form's action attribute you'll enter the name of your servlet.
2. Create a servlet called ProcessForm.java. The servlet will retrieve the parameters from the form. It will then display them on a page called output.jsp.

**DO NOT USE BOOTSTRAP**. You do not get points for beauty. Functionality is important here. The sole purpose of this project is to have you create a minimal servlet/form processor, not a fancy website. That comes later.

####Your form MUST use each of the following HTML form elements:
```html
<form> Defines an HTML form for user input. Be sure to set the action attribute to your servlet's ```@WebServlet``` annotation 
<input> Defines an input control. It must have a type attribute. And a name attribute. 
<textarea> Defines a multiline input control (text area)
<label> Defines a label for an <input> element
<select> Defines a drop-down list
<optgroup> Defines a group of related options in a drop-down list
<option> Defines an option in a drop-down list
<submit>Defines a form submit button
```