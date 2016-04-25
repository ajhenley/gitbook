HTML (HyperText Markup Language) is the primary markup language used in web pages. Web pages consist of content like text and images as well as markup (tags). The markup is a series of tags. The browser renders the tags to control how the contents get displayed.  HTML was originally designed as a language for describing scientific documents. It has since adapted to describe other types of documents and even applications.

HTML formats the layout of most web pages. It can specify how headings, paragraphs, tables and lists should display. The markup can specify which parts of text should be bold, italic or underlined. It can specify font colors and settings.  HTML files contain both the content (primary text) and formatting (markup). 

####Before we start

To create and test HTML pages, you will need an editor and a web browser. HTML can be edited in any plain text editor. Ideally, use one that highlights HTML markup with colors to make it easier to read. Common plain text editors include Notepad (or Notepad++) for Microsoft&reg; Windows, TextEdit for Mac, and Kate, Gedit, Vim, and Emacs for Linux.

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
<!DOCTYPE html>
<html>
  <head>
    <title>Simple document</title>
  </head>
  <body>
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

####General HTML tag code style
* Most tags must be written in pairs between which the effects of the tag will be applied.
** <nowiki><em>This text is emphasized</em></nowiki> &#8211; <em>This text is emphasized</em>
** <nowiki>This text includes <code>computer code</code></nowiki> &#8211; This text includes <code>computer code</code>
** <nowiki><em>This text is emphasized and has <code>computer code</code></em></nowiki> &#8211; <em>This text is emphasized and has <code>computer code</code></em><br>
* HTML tag pairs must be aligned to encapsulate other tag pairs, for example:
** <nowiki><code><em>This text is both code and emphasized</em></code></nowiki> &#8211; <code><em>This text is both code and emphasized</em></code><br>
** <strong>A mistake: </strong><nowiki><em><code>This markup is erroneous</em></code></nowiki>

####The &lt;html&gt; Tag

The <html> and </html> tags are used to mark the beginning and end of an HTML document. This tag does not have any effect on the appearance of the document.<br>
This tag is used to make browsers and other programs know that this is an HTML document.<br><br>
'''Useful attributes:'''<br>
;dir attribute
:This attribute specifies in which manner the browser will present text within the entire document. It can have values of either ''ltr'' (left to right) or ''rtl'' (right to left). By default this is set to ltr. Generally rtl is used for languages like Persian, Chinese, Hebrew, Urdu etc.
<u>Example:</u> &lt;html dir="ltr"&gt;

;lang attribute<br>
:The lang attribute generally specifies which language is being used within the document.<br>
Special types of codes are used to specify different languages:<br>
en - English<br>
fa - Farsi<br>
fr - French<br>
de - German<br>
it - Italian<br>
nl - Dutch<br>
el - Greek<br>
es - Spanish<br>
pt - Portuguese<br>
ar - Arabic<br>
he - Hebrew<br>
ru - Russian<br>
zh - Chinese<br>
ja - Japanese<br>
hi - Hindi<br>

