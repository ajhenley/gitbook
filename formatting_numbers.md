# Formatting numbers

   <h3>Formatting Numbers</h3>
<p>Use the NumberFormat class:</p>
<p><a href="http://docs.oracle.com/javase/7/docs/api/java/text/NumberFormat.html" class="external" target="_blank"><span><span>http://docs.oracle.com/javase/7/docs/api/java/text/NumberFormat.html</span><span class="screenreader-only">&nbsp;(Links to an external site.)</span></span><span class="ui-icon ui-icon-extlink ui-icon-inline" title="Links to an external site."></span></a></p>
<p>&nbsp;</p>
<h3>Here are two articles on formatting strings for printing.</h3>
<p><a href="https://docs.oracle.com/javase/tutorial/java/data/numberformat.html" class="external" target="_blank"><span><span>https://docs.oracle.com/javase/tutorial/java/data/numberformat.html</span><span class="screenreader-only">&nbsp;(Links to an external site.)</span></span><span class="ui-icon ui-icon-extlink ui-icon-inline" title="Links to an external site."></span></a></p>
<p><a href="http://examples.javacodegeeks.com/core-java/lang/string/java-string-format-example/" class="external" target="_blank"><span><span>http://examples.javacodegeeks.com/core-java/lang/string/java-string-format-example/</span><span class="screenreader-only">&nbsp;(Links to an external site.)</span></span><span class="ui-icon ui-icon-extlink ui-icon-inline" title="Links to an external site."></span></a></p>
<h3></h3>
<h3>String formatting</h3>
<ul>
<li>
<code>%s</code> &nbsp; &nbsp; &nbsp; : will print the string as it is.</li>
<li>
<code>%15s</code> &nbsp; &nbsp;: will <span>print</span> the string as it is. If the string has less than 15 characters, the output will be padded on the left.</li>
<li>
<code>%-6s </code>&nbsp;: will <span>print</span> the string as it is. If the string has less than 6 characters, the output will be padded on the right.</li>
<li>
<code>%.8d</code> : will print maximum 8 characters of the string.</li>
</ul>
<h3>Integer formatting</h3>
<ul>
<li>
<code>%d</code> &nbsp; &nbsp; &nbsp; : will print the integer as it is.</li>
<li>
<code>%6d</code> &nbsp; &nbsp;: will <span>print</span> the integer as it is. If the number of digits is less than 6, the output will be padded on the left.</li>
<li>
<code>%-6d </code>&nbsp;: will <span>print</span> the integer as it is. If the number of digits is less than 6, the output will be padded on the right.</li>
<li>
<code>%06d</code> : will <span>print</span> the integer as it is. If the number of digits is less than 6, the output will be padded on the left with zeroes.</li>
<li>
<code>%.2d</code> : will print maximum 2 digits of the integer.</li>
</ul>
  