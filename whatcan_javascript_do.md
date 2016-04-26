<p><span>JavaScript is most commonly used as a client side scripting language. This means that JavaScript code is written into an HTML page. When a user requests an HTML page with JavaScript in it, the script is sent to the browser and it's up to the browser to do something with it. The browser contains a JavaScript engine that processes the JavaScript so the server does not have to.</span></p>
<p>One of the big issues with JavaScript is to make sure that your page works no matter what browser is being used.A great resource for checking browser compatibility is <a id="" class="" title="" href="http://browsershots.org/" target="">http://browsershots.org/</a>.</p>
<p>The document object model (DOM) is a collection of nodes in the web browser's memory that represent the current web page. The nodes are organized as a hirearchy. When the DOM is changed the web browser immediately displays the results of the change.</p>
<p>&nbsp;</p>
<h3>JavaScript Can't ...</h3>
<ul>
<li>Read or write files</li>
<li>Communicate over the network</li>
<li>Run other programs</li>
</ul>
<h3>JavaScript can ...</h3>
<ul>
<li>Change HTML content and attributes by modifying the DOM (document object model) of the web page</li>
<li>Create dynamic menus</li>
<li>Validate data in a form before it is sent to the server for processing</li>
<li>Respond to user actions such as mouse clicks and key presses</li>
<li>Animate elements in a web page</li>
<li>Change a CSS style sheet that a web page uses</li>
<li>Sort the data in a table</li>
<li>Change images when the user rolls the mouse over it</li>
<li>Prompt the user</li>
</ul>


####JavaScript Example
In the example below I have added two paragraph tags with their id attribute set. That helps JavaScript identify the tags. Then as the page is loading the web server comes across the script tags which means the web server will execute the code in that script. So it tells JavaScript to set the value of each identified element to the value indicated. The Date() function returns the current date and tinme.
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Title of the document</title>
</head>

<body>
    
<p id="greeting"></p>
<p id="date"></p>
<!--JavaScript can set content for your page-->
<script>
    document.getElementById("greeting").innerHTML = "Hello JavaScript";
    document.getElementById("date").innerHTML = Date();
</script>
</body>

</html>
```