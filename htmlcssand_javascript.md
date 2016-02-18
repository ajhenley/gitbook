###HTML,CSS and Javascript

The HTML (HyperText Markup Language) is used in most pages of the World Wide Web. HTML files contain both the primary text content and additional formatting markup, i.e. sequences of characters that tell web browsers how to display and handle the main content. The markup can specify which parts of text should be bold, where the headings are, or where tables, table rows, and table cells start and end. Though most commonly displayed by a visual web browser, HTML can also be used by browsers that generate audio of the text, by braille readers that convert pages to a braille format, and by accessory programs such as email clients.

####Before we start

To author and test HTML pages, you will need an editor and a web browser. HTML can be edited in any plain text editor. Ideally, use one that highlights HTML markup with colors to make it easier to read. Common plain text editors include Notepad (or Notepad++) for Microsoft&reg; Windows, TextEdit for Mac, and Kate, Gedit, Vim, and Emacs for Linux.

Many others editors exist with a wide range of features. While some offer WYSIWYG (''what you see is what you get'') functionality, that means hiding the markup itself and having to auto-generate it. WYSIWYG options are never as clean or transparent or as useful for learning compared with real code-based text editors.

To preview your documents, you'll need a web browser. To assure most viewers will see good results, ideally you will test your documents in several browsers. Each browser has slightly different rendering and particular quirks.

The most common browsers include Microsoft Internet Explorer, Google Chrome, Mozilla Firefox, Safari, and Opera. To assure that your documents are readable in a text-only environment, you can test with Lynx.<!--Do not provide web link for Lynx only, so comment out:with a Windows version of Lynx is available at http://csant.info/lynx.htm.-->

####A simple document
Let's start with a simple document. Write this code in your editor (or copy-and-paste it), and save it as "index.html" or "index.htm".  The file must be saved with the exact extension, or it will not be rendered correctly.

<!--
 Please keep this example to the bare minimum needed to validate as HTML5.
 All element names should be in lowercase and all optional tags should be present.
 No attributes should be used.
 Additional features can be introduced in later sections.
-->
```html
<source lang="html5">
<!DOCTYPE html>
<html>
  <head>
    <title>Simple document</title>
  </head>
  <body>
    <p>This is some text in a paragraph that will be seen by viewers.</p>
  </body>
</html>
</source>
```

Now open the document in your browser and look at the result. From the above example, we can deduce certain essentials of an HTML document:
* The first line with <code>&lt;!DOCTYPE html&gt;</code> declares the type of the document.
* The HTML document begins with a <code>&lt;html&gt;</code> tag and ends with its counterpart, the <code>&lt;/html&gt;</code> tag.
* Within the <code>&lt;html&gt;&lt;/html&gt;</code> tags, there are two main pairs of tags, <code>&lt;head&gt;&lt;/head&gt;</code> and <code>&lt;body&gt;&lt;/body&gt;</code>.
* Within the <code>&lt;head&gt;&lt;/head&gt;</code> tags, there are the <code>&lt;title&gt;&lt;/title&gt;</code> tags which enclose the textual title to be shown in the title bar of the web browser.
* Within the <code>&lt;body&gt;&lt;/body&gt;</code> is a paragraph marked by a <code>&lt;p&gt;&lt;/p&gt;</code> tag pair.
