HTML (HyperText Markup Language) is the primary markup language used in web pages. Web pages consist of content like text and images as well as markup (tags). The markup is a series of tags. The browser renders the tags to control how the contents get displayed.  HTML was originally designed as a language for describing scientific documents. It has since adapted to describe other types of documents and even applications.

HTML formats the layout of most web pages. It can specify how headings, paragraphs, tables and lists should display. The markup can specify which parts of text should be bold, italic or underlined. It can specify font colors and settings.  HTML files contain both the content (primary text) and formatting (markup). 

####Before we start

To create and test HTML pages, you only need a text editor and a web browser. Notepad++ or GEdit or Kate will work for our purposes because they highlight HTML markup with colors to make it easier to read. 

To preview your documents, you'll need a web browser. To assure most viewers will see good results, ideally you should test your documents in different browsers. Each browser has slightly different rendering and other quirks. The most common browsers include Google Chrome, Mozilla Firefox, Microsoft Internet Explorer, Safari, and Opera. 

####A simple document
Let's start with a simple document. Write this code in your editor (or copy-and-paste it), and save it as "index.html".  The file must be saved with the exact extension, or it will not be rendered correctly.

<!--
 Please keep this example to the bare minimum needed to validate as HTML5.
 All element names should be in lowercase and all optional tags should be present.
 No attributes should be used.
 Additional features can be introduced in later sections.
-->
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Simple document</title>
  </head>
  <body>
    <h1>This is my heading</h1>
    <p>This is some text in a paragraph that will be seen by viewers.</p>
  </body>
</html>
```

Now open the document in your browser and look at the result. From the above example, we can deduce certain essentials of an HTML document:
* The first line with <code>&lt;!DOCTYPE html&gt;</code> declares the type of the document.
* The HTML document begins with a <code>&lt;html&gt;</code> tag and ends with its counterpart, the <code>&lt;/html&gt;</code> tag.
* Within the <code>&lt;html&gt;&lt;/html&gt;</code> tags, there are two main pairs of tags, <code>&lt;head&gt;&lt;/head&gt;</code> and <code>&lt;body&gt;&lt;/body&gt;</code>.
* Within the <code>&lt;head&gt;&lt;/head&gt;</code> tags, there are the <code>&lt;title&gt;&lt;/title&gt;</code> tags which enclose the textual title to be shown in the title bar of the web browser.
* Within the <code>&lt;body&gt;&lt;/body&gt;</code> is a paragraph marked by a <code>&lt;p&gt;&lt;/p&gt;</code> tag pair.

