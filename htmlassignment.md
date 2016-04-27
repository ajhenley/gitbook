<!--djw
todo: add steps to create dynamic web application in eclipse and to add, then view a web page 
-->
###A basic web page

Create a basic web page with a title and a header tag that both say, "Hello World!"

All well-designed HTML pages meets HTML5 standards. This means it has the basic structure shown below. The ```<!DOCTYPE>``` declaration the first thing in your HTML document. The ```<!DOCTYPE>``` declaration is not actually an HTML tag but rather an instruction to the  browser.


Every tag must have a corresponding closing tag. Sometimes you'll see tags that open and close with two tags, ```<p>...</p>``` and sometimes with just one, ```<br/>```. Both forms are correct. The latter form has no content. It simply tells the browser to insert a line break at that spot.

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Dalton Used Car Emporium</title>
</head>

<body>
<p>Hello, World!</p>
</body>

</html>
```

####Your assignment
You're going to work with web projects now. No more Java console applications.
From Eclipse, follow the following menu items: File | New | Other | Web | Static Web Project.  On the next form that comes up in Eclipse enter the project name and select the target runtime. For the target runtime select HTTP Preview. You may have to click the New Runtime button to select HTTP Preview.

In Eclipse create a new HTML page called index.html. Simply copy the above html code from above into this page. Also header just below the ```<body``` tag that says "Welcome". ```<h1>Welcome</h1>```. Copy that tag three times below the first one and change "h1" to "h2", "h3" and "h4". What happens?

