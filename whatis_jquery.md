###What is JQuery?

jQuery is a JavaScript library. jQuery takes a lot of common tasks that require many lines of JavaScript code to accomplish, and wraps them into methods that you can call with a single line of code. jQuery handles the complexity behind HTML document traversal and manipulation even across multiple browsers. The purpose of jQuery is to make it much easier to use JavaScript on your website.
What can you do with jQuery?
 * HTML/DOM manipulation
 * CSS manipulation
 * HTML event methods
 * Effects and animations

####Include jQuery in your web page
```html
<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
```
 
####$( document ).ready()
A page can't be manipulated safely until the document is "ready." jQuery detects this state of readiness for you. Code included inside ```$( document ).ready()``` will only run once the page Document Object Model (DOM) is ready for JavaScript code to execute. Code included inside ```$( window ).load(function() { ... })``` will run once the entire page (images or iframes), not just the DOM, is ready.

```html
// A $( document ).ready() block.
$( document ).ready(function() {
    console.log( "ready!" );
});
```

####Putting jQuery Into No-Conflict Mode
When you put jQuery into no-conflict mode, you have the option of assigning a new variable name to replace the $ alias. By default, jQuery uses $ as a shortcut for jQuery. Thus, if you are using another JavaScript library that uses the $ variable, you can run into conflicts with jQuery. In order to avoid these conflicts, you need to put jQuery in no-conflict mode immediately after it is loaded onto the page and before you attempt to use jQuery in your page.

```html
<!-- Putting jQuery into no-conflict mode. -->
<script src="prototype.js"></script>
<script src="jquery.js"></script>
<script>
 
var $j = jQuery.noConflict();
// $j is now an alias to the jQuery function; creating the new alias is optional.
 
$j(document).ready(function() {
    $j( "div" ).hide();
});
```
