<!-- need an image showing DOM nodes -->
# Explore the DOM with JavaScript

With the HTML DOM, JavaScript can access and change all the elements of an HTML document.

When a web page is loaded, the browser creates a Document Object Model of the page.

The HTML DOM model is constructed as a tree of Objects:

The HTML DOM is a standard object model and programming interface for HTML. It defines:

The HTML elements as objects
The properties of all HTML elements
The methods to access all HTML elements
The events for all HTML elements
In other words: The HTML DOM is a standard for how to get, change, add, or delete HTML elements.

Add the following script to your crabcake web page. When you click on the button the script will list all the elements in the DOM for your web page. Add another tag and run the script again. You should see your new tag.

The script should be placed between the <head> and </head> tags.

<script language="JavaScript">
<!--
function listTags()
{
 var tag, tags;
 // or you can use var allElem=document.all; and loop on it
 tags = "The tags in the page are:"
 for(i = 0; i < document.all.length; i++)
 {
   tag = document.all(i).tagName;
   tags = tags + "<br/>" + tag;
 }
 document.write(tags);
}// -->
</script>
 

Also, add the following button to your page so the function will run when the button is clicked.

<button onclick="listTags()">List my Tags</button>