# Formatting prices with two decimal places

<h1 class="page-title">Formatting Prices with Two Decimal Places</h1>
  
    <pre class="lang-java prettyprint prettyprinted"><code><span class="typ">You can use the NumberFormat class from the Java API<br><br>NumberFormat</span><span class="pln"> nf</span><span class="pun">=</span><span class="pln"> </span><span class="typ">NumberFormat</span><span class="pun">.</span><span class="pln">getInstance</span><span class="pun">();</span><span class="pln">
nf</span><span class="pun">.</span><span class="pln">setMaximumFractionDigits</span><span class="pun">(</span><span class="lit">2</span><span class="pun">);</span><span class="pln">
nf</span><span class="pun">.</span><span class="pln">setMinimumFractionDigits</span><span class="pun">(</span><span class="lit">2</span><span class="pun">);</span><span class="pln">
nf</span><span class="pun">.</span><span class="pln">setRoundingMode</span><span class="pun">(</span><span class="typ">RoundingMode</span><span class="pun">.</span><span class="pln">HALF_UP</span><span class="pun">);</span><span class="pln">

</span><span class="typ">System</span><span class="pun">.</span><span class="pln">out</span><span class="pun">.</span><span class="pln">print</span><span class="pun">(</span><span class="pln">nf</span><span class="pun">.</span><span class="pln">format</span><span class="pun">(</span><span class="pln">decimalNumber</span><span class="pun">));<br><br>Or you can use String.format. This will also work with printf to print a formatted string.<br></span></code></pre>
<pre class="lang-java prettyprint prettyprinted"><code><span class="kwd">double</span><span class="pln"> d </span><span class="pun">=</span><span class="pln"> yourDoubleValue</span><span class="pun">;</span><span class="pln">  
</span><span class="typ">String</span><span class="pln"> formattedData </span><span class="pun">=</span><span class="pln"> </span><span class="typ">String</span><span class="pun">.</span><span class="pln">format</span><span class="pun">(</span><span class="str">"%.02f"</span><span class="pun">,</span><span class="pln"> d</span><span class="pun">);</span></code></pre>
<pre class="lang-java prettyprint prettyprinted"><code><span class="pun">&nbsp;</span></code></pre>
  
</div>