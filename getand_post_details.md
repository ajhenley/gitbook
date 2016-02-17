###Get and Post Details

You can download this project from GitHub. It will show you the results of submitting a form via Get and via Post. The index page contains two forms. The only difference between the two forms is one sends its data via get and the other via post. Open this project in Eclipse. Once you run it you will get a better understanding of Get and Post and the Request object which comes from the browser. 

The GET method sends form information via the URL. When using the GET method the 3rd section of the request packet, the request body, remains empty.

The POST method is used when you create an HTML form, and request method=POST as part of the tag. The POST method allows the client to send form data to the server in the request body section of the request. The data is encoded and is formatted similar to the GET method. The data is sent to the server via standard input.

 

An HTML5 document looks like this:

```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8"/>
<link href="css/some-stylesheet.css"
      rel="stylesheet"/>
<script src="scripts/some-script.js">
</script>
</head>
<body>
...
</body>
</html>
``

Within that document you can create a form to submit data to the web server. The form goes between the <body> and </body> tags. Our web server is Tomcat. A servlet is a program which extends Tomcat. The servlet gives Tomcat the ability to handle the url in the @WebServlet annotation at the top of your servlet code file.

The form can send its data via either GET or POST. Those are the only two choices.  GET sends the data in the URL. POST sends the data as the body of the request packet. The above application illustrates the difference.

A proper form contains the following
* An opening Form tag with an action attribute and a method attribute.
* Any number of inputs each of which must have name attributes identifying the name by which request. getParameter will refer to each
* Labels to identify the inputs for the user
* A submit button which will tell the browser to send the value of each input along with its name to the servlet for processing
* A closing form tag
 

The hidden input below can be used to help the servlet determine which form was submitted.

<form action="emailList" method="post">
<!-- hidden input to let servlet know which form was used -->
 <input type="hidden" name="hiddenAction" value="add">
<label>Email:</label>
 <input type="email" name="email" required><br>

<label>First Name:</label>
 <input type="text" name="firstName" required><br>

<label>Last Name:</label>
 <input type="text" name="lastName" required><br>

<label>&nbsp;</label>
 <input type="submit" value="Join Now" id="submit">
 </form>
</body>
</html>
 