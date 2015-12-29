###Formatting prices with two decimal places
You can use the NumberFormat class from the Java API
NumberFormat nf = NumberFormat.getInstance();
nf.setMaximumFractionDigits(2);
nf.setMinimumFractionDigits(2);
setRoundingMode(RoundingMode.HALF_UP);

System.out.print(nf.format(decimalNumber));
class="pln">nf</span><span class="pun">.</span><span class="pln">format</span><span class="pun">(</span><span class="pln">decimalNumber</span><span class="pun">));<br><br>Or you can use String.format. This will also work with printf to print a formatted string.<br></span></code></pre>
<pre class="lang-java prettyprint prettyprinted"><code><span class="kwd">double</span><span class="pln"> d </span><span class="pun">=</span><span class="pln"> yourDoubleValue</span><span class="pun">;</span><span class="pln">  
</span><span class="typ">String</span><span class="pln"> formattedData </span><span class="pun">=</span><span class="pln"> </span><span class="typ">String</span><span class="pun">.</span><span class="pln">format</span><span class="pun">(</span><span class="str">"%.02f"</span><span class="pun">,</span><span class="pln"> d</span><span class="pun">);</span></code></pre>
<pre class="lang-java prettyprint prettyprinted"><code><span class="pun">&nbsp;</span></code></pre>
  
</div>