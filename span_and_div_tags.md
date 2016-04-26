###Span and Div Tags
* The &lt;span&gt; tag is used to group inline-elements in a document.
* The &lt;span&gt; tag provides no visual change by itself.
* The &lt;span&gt; tag provides a way to control the style of part of your document.

* The &lt;div&gt; tag defines a section of an HTML document.
* The &lt;div&gt; tag is used to group elements to format them with CSS.
* You can make a &lt;span&gt; or &lt;div&gt; point to a style sheet using the ```id``` or ```class``` attribute.
* The ```id``` must be unique. There can only be one element with that particular id.
* The ```class``` attribute can apply to in different elements.
 

```html
<span style="color:ff0000">This text is red</span> this text isn't red.
<div style="color:#0000ff">
  <h3>This is a heading</h3>
  <p>This is a paragraph.</p>
</div>
```

The &lt;span&gt; and &lt;div&gt; tags have no required attributes, but the three that are the most useful are:
* **style** - specifies a style that applies to all content and elements up to the end tag
* **class** - specifies a CSS classs that applies to all content and elements up to the end tag
* **id** - identifies the tag so you can select it with jQuery or JavaScript

In general, use <code>id</code> whenever you want to refer to a specific element and <code>class</code> when you have a number of things that are all alike. 

