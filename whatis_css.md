# What is CSS?
<h2 class="entry-title">INLINE VS INTERNAL VS EXTERNAL&nbsp;CSS</h2>
<div class="entry-content">
<h2>What is CSS</h2>
<div>CSS&nbsp;stands for&nbsp;<strong>C</strong>ascading&nbsp;<strong>S</strong>tyle&nbsp;<strong>S</strong>heets. It&rsquo;s a style sheet which defines&nbsp;<strong>how to display</strong>&nbsp;HTML elements. <strong>CSS</strong>&nbsp;<strong>solves the problem&nbsp;</strong>of designing same thing again and again which little modifications.&nbsp;</div>
<h2>Types of CSS</h2>
<div>There are ways to do Designing/CSS that are known as:</div>
<ol>
<li>Inline CSS</li>
<li>Internal CSS</li>
<li>External CSS</li>
</ol>
<div>Let me give a small example of each to understand it better.</div>
<h4>Inline CSS</h4>
<div>An inline style loses many of the advantages of style sheets by mixing content with presentation. Use this method sparingly!&nbsp;To use inline styles you use the style attribute in the relevant tag. The style attribute can contain any CSS property. The example shows how to change the color and the left margin of a paragraph:</div>
<p><br />&lt;p style="color: sienna; margin-left: <span>20px&rdquo;&gt;This is a paragraph.&lt;/p&gt;</span></p>
<p>would show the paragraph as</p>
<p>This is a paragraph.</p>
<h4>Internal CSS</h4>
<div>An internal style sheet should be used when a single document has a unique style. You define internal styles in the head section of an HTML page, by using the &lt;style&gt; tag, like this:</div>
<p>&lt;head&gt;</p>
<p>&lt;style&gt;</p>
<p>hr {color:sienna;}</p>
<p>p {margin-left:20px;}</p>
<p>body {background-image:url(&ldquo;images/back40.gif&rdquo;);}</p>
<p>&lt;/style&gt;</p>
<p>&lt;/head&gt;</p>
<h4>External CSS</h4>
<div>An external style sheet is ideal when the style is applied to many pages. With an external style sheet, you can change the look of an entire Web site by changing one file. Each page must link to the style sheet using the &lt;link&gt; tag. The &lt;link&gt; tag goes inside the head section:</div>
<p>&lt;head&gt;</p>
<p>&lt;link type="css" href="<span class="skimlinks-unlinked">mystyle.css"</span>&nbsp;/&gt;</p>
<p>&lt;/head&gt;</p>
<div>An external style sheet can be written in any text editor. The file should not contain any html tags. Your style sheet should be saved with a .css extension. An example of a style sheet file is shown below:</div>
<p>hr {color:sienna;}</p>
<p>p {margin-left:20px;}</p>
<p>body {background-image:url(&ldquo;images/back40.gif&rdquo;);}</p>
<h2>Which one to use?</h2>
<div>The major question is which CSS would be used. After going through many web sites and articles, I am here writing my views.</div>
<h4>Inline CSS</h4>
<div><strong>Advantages:</strong></div>
<div>Inline CSS can be used for many purposes, some of which include:</div>
<ol>
<li><strong>Testing: &nbsp;</strong>Many web designers use Inline CSS when they begin working on new projects, this is because its easier to scroll up in the source, rather than change the source file.&nbsp;Some also using it to debug their pages, if they encounter a problem which is not so easily fixed. This can be done in combination with the Important rule of CSS.</li>
<li><strong>Quick-fixes:</strong>There are times where you would just apply a direct fix in your HTML source, using the style attribute, but you would usually move the fix to the relevant files when you are either able, or got the time.</li>
<li><strong>Smaller Websites: </strong>The website such as Blogs where there are only limited number of pages, using of Inline CSS helps users and service provider.</li>
<li><strong>Lower the HTTP Requests</strong>: The major&nbsp;benefit of using Inline CSS is lower HTTP Requests which means the website loads faster than External CSS.</li>
</ol>
<div><strong>Disadvantages</strong></div>
<div>Inline CSS some of the disadvantages of which includes:</div>
<ol>
<li><strong>Overriding</strong>:&nbsp;Because they are the most specific in the cascade, they can over-ride things you didn&rsquo;t intend them to.</li>
<li><strong>Every Element</strong>: Inline styles must be applied to every element you want them on. So if you want all your paragraphs to have the font family &ldquo;Arial&rdquo; you have to add an inline style to each &lt;p&gt;&nbsp;tag in your document. This adds both maintenance work for the designer and download time for the reader.</li>
<li><strong>Pseudo-elements</strong>: It&rsquo;s impossible to style pseudo-elements and classes with inline styles. For example, with external and internal style sheets, you can style the visited, hover, active, and link color of an anchor tag. But with an inline style all you can style is the link itself, because that&rsquo;s what the style attribute is attached to.</li>
</ol>
<h4>Internal CSS</h4>
<div><strong>Advantages</strong></div>
<div>Since the Internal CSS have more&nbsp;preference&nbsp;over Inline CSS. There are&nbsp;numerous advantages of which some of important are an under:</div>
<ol>
<li><strong>Cache Problem</strong>: Internal styles will be read by all browsers unless they are hacked to hide from certain ones. This removes the ability to use media=all or @import to hide styles from old, crotchety browsers like IE4 and NN4.</li>
<li><strong>Pseudo-elements</strong>: It&rsquo;s impossible to style pseudo-elements and classes with inline styles. With Internal style sheets, you can style the visited, hover, active, and link color of an anchor tag.</li>
<li><strong>One style of same element</strong>:&nbsp;Internal styles need not be applied to every element. So if you want all your paragraphs to have the font family &ldquo;Arial&rdquo; you have to add an Inline style &lt;p&gt;&nbsp;tag in Internal Style document.</li>
<li><strong>No additional downloads</strong>:&nbsp;No additional downloads necessary to receive style information or we have less HTTP Request</li>
</ol>
<div><strong>Disadvantages</strong></div>
<ol>
<li><strong>Multiple Documents</strong>: This method can&rsquo;t be used, if you want to use it on multiple web pages.</li>
<li><strong>Slow Page Loading</strong>: As there are less HTTP Request but by using the Internal CSS the page load slow as&nbsp;compared&nbsp;to Inline and External CSS.</li>
<li><strong>Large File Size:&nbsp;</strong><span>While using the Internal CSS the page size increases but it helps only to Designers while working offline but when the website goes online it consumers much time as&nbsp;compared&nbsp;to offline.</span></li>
</ol>
<h4>External CSS</h4>
<div><strong>Advantages</strong></div>
<div>There are many advantages for using external CSS and some of are:</div>
<ol>
<ol>
<li><strong>Full Control of page structure</strong>: CSS allows you to display your web page according to W3C HTML standards without making any compromise with the actual look of the page. Google is the leading search Engine and major source of traffic. Google gives very little value to the web pages that are well-organized, since the value is little thus many Designers ignore it. But by taking small value may drive much traffic to the website.</li>
<li><strong>Reduced file-size</strong>: By including the styling of the text in a separate file, you can dramatically decrease the file-size of your pages. Also, the content-to-code ratio is far greater than with simple HTML pages, thus making the page structure easier to read for both the programmer and the spiders. With CSS you can define the visual effect that you want to apply to images, instead of using images per say. The space you gain this way can be used for text that is relevant for spiders (i.e. keywords), and you will also lower the file-size of the page.</li>
<li><strong>Less load time</strong>: Today, when Google has included the Loading time in his algorithm, its become more important to look into the page loading time and another benefit of having low file-size pages translates into reduced bandwidth costs. CSS can help you save some money by offering you. I done a small experiment to check the page load time. I am using the Mobile Internet Connection for testing and for that first I cleared the web cache of the website and visited&nbsp;for first time after clearing cache. The total time taken to load the website is 16 seconds. Now I hit the F5 button and the time taken to load the website is 8 seconds. Using external CSS has reduced the page load timing. It me explain it how it reduces the time, when you first visited the website, it has downloaded all the contents + external CSS and while downloading external CSS, it has marked the CSS with the time stamp with the time stamp of the web server. Now when you hit F5, it again starts working but this time the browser compare the time stamps of downloaded CSS with Web Server CSS and due to same time stamp, it doesn&rsquo;t downloaded the CSS external file from server and using the already downloaded time, which make the Web Page Loading time faster as com paired to first time. If you check under Firebug or Chrome tools it will tell 304 Not Modified, meaning the file is not modified since last downloaded file, and thus ignoring to download the external CSS file.</li>
</ol>
</ol>
<div></div>
</div>
