<!--djw
todo: add steps to create dynamic web application in eclipse and to add, then view a web page 
-->
Create a basic web page with a title and a header tag that both say, "Hello World!"

All well-designed HTML pages must be formatted to meet HTML5 standards. Which means it must have the basic structure shown below. The first line must be the ```DOCTYPE``` tag. Every tag must have a corresponding closing tag. Sometimes you'll see tags that open and close with two tags, ```<p>...</p>``` and sometimes with just one, ```<br/>```. Both forms are correct. The latter form has no content. It simply tells the browser to insert a line break at that spot.

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Title of the document</title>
</head>

<body>
<p>Content of the document....</p>
</body>

</html>
```

####Create a Static Web Project in Eclipse
You're going to work with static web projects now.
From Eclipse, follow the following menu items: File | New | Other | Web | Static Web Project.  On the next form that comes up in Eclipse enter the project name and select the target runtime. For the target runtime select HTTP Preview. You may have to click the New Runtime button to select HTTP Preview.

