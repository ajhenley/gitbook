# Coding arithmetic statements

<h1 class="title">Mathematical Operations</h1>
<p>Now that we know how to declare and initialize variables in Java, we can do some mathematics with those variables.</p>
<pre class="code java literal-block"><span class="ln"> 1 </span><span class="keyword declaration">public</span> <span class="keyword declaration">class</span> <span class="name class">MathOperations</span>
<span class="ln"> 2 </span><span class="operator">{</span>
<span class="ln"> 3 </span>    <span class="keyword declaration">public</span> <span class="keyword declaration">static</span> <span class="keyword type">void</span> <span class="name function">main</span><span class="operator">(</span> <span class="name">String</span><span class="operator">[]</span> <span class="name">args</span> <span class="operator">)</span>
<span class="ln"> 4 </span>    <span class="operator">{</span>
<span class="ln"> 5 </span>        <span class="keyword type">int</span> <span class="name">a</span><span class="operator">,</span> <span class="name">b</span><span class="operator">,</span> <span class="name">c</span><span class="operator">,</span> <span class="name">d</span><span class="operator">,</span> <span class="name">e</span><span class="operator">,</span> <span class="name">f</span><span class="operator">,</span> <span class="name">g</span><span class="operator">;</span>
<span class="ln"> 6 </span>        <span class="keyword type">double</span> <span class="name">x</span><span class="operator">,</span> <span class="name">y</span><span class="operator">,</span> <span class="name">z</span><span class="operator">;</span>
<span class="ln"> 7 </span>        <span class="name">String</span> <span class="name">one</span><span class="operator">,</span> <span class="name">two</span><span class="operator">,</span> <span class="name">both</span><span class="operator">;</span>
<span class="ln"> 8 </span>
<span class="ln"> 9 </span>        <span class="name">a</span> <span class="operator">=</span> <span class="literal number integer">10</span><span class="operator">;</span>
<span class="ln">10 </span>        <span class="name">b</span> <span class="operator">=</span> <span class="literal number integer">27</span><span class="operator">;</span>
<span class="ln">11 </span>        <span class="name">System</span><span class="operator">.</span><span class="name attribute">out</span><span class="operator">.</span><span class="name attribute">println</span><span class="operator">(</span> <span class="literal string">"a is "</span> <span class="operator">+</span> <span class="name">a</span> <span class="operator">+</span> <span class="literal string">", b is "</span> <span class="operator">+</span> <span class="name">b</span> <span class="operator">);</span>
<span class="ln">12 </span>
<span class="ln">13 </span>        <span class="name">c</span> <span class="operator">=</span> <span class="name">a</span> <span class="operator">+</span> <span class="name">b</span><span class="operator">;</span>
<span class="ln">14 </span>        <span class="name">System</span><span class="operator">.</span><span class="name attribute">out</span><span class="operator">.</span><span class="name attribute">println</span><span class="operator">(</span> <span class="literal string">"a+b is "</span> <span class="operator">+</span> <span class="name">c</span> <span class="operator">);</span>
<span class="ln">15 </span>        <span class="name">d</span> <span class="operator">=</span> <span class="name">a</span> <span class="operator">-</span> <span class="name">b</span><span class="operator">;</span>
<span class="ln">16 </span>        <span class="name">System</span><span class="operator">.</span><span class="name attribute">out</span><span class="operator">.</span><span class="name attribute">println</span><span class="operator">(</span> <span class="literal string">"a-b is "</span> <span class="operator">+</span> <span class="name">d</span> <span class="operator">);</span>
<span class="ln">17 </span>        <span class="name">e</span> <span class="operator">=</span> <span class="name">a</span><span class="operator">+</span><span class="name">b</span><span class="operator">*</span><span class="literal number integer">3</span><span class="operator">;</span>
<span class="ln">18 </span>        <span class="name">System</span><span class="operator">.</span><span class="name attribute">out</span><span class="operator">.</span><span class="name attribute">println</span><span class="operator">(</span> <span class="literal string">"a+b*3 is "</span> <span class="operator">+</span> <span class="name">e</span> <span class="operator">);</span>
<span class="ln">19 </span>        <span class="name">f</span> <span class="operator">=</span> <span class="name">b</span> <span class="operator">/</span> <span class="literal number integer">2</span><span class="operator">;</span>
<span class="ln">20 </span>        <span class="name">System</span><span class="operator">.</span><span class="name attribute">out</span><span class="operator">.</span><span class="name attribute">println</span><span class="operator">(</span> <span class="literal string">"b/2 is "</span> <span class="operator">+</span> <span class="name">f</span> <span class="operator">);</span>
<span class="ln">21 </span>        <span class="name">g</span> <span class="operator">=</span> <span class="name">b</span> <span class="operator">%</span> <span class="literal number integer">10</span><span class="operator">;</span>
<span class="ln">22 </span>        <span class="name">System</span><span class="operator">.</span><span class="name attribute">out</span><span class="operator">.</span><span class="name attribute">println</span><span class="operator">(</span> <span class="literal string">"b%10 is "</span> <span class="operator">+</span> <span class="name">g</span> <span class="operator">);</span>
<span class="ln">23 </span>
<span class="ln">24 </span>        <span class="name">x</span> <span class="operator">=</span> <span class="literal number float">1.1</span><span class="operator">;</span>
<span class="ln">25 </span>        <span class="name">System</span><span class="operator">.</span><span class="name attribute">out</span><span class="operator">.</span><span class="name attribute">println</span><span class="operator">(</span> <span class="literal string">"\nx is "</span> <span class="operator">+</span> <span class="name">x</span> <span class="operator">);</span>
<span class="ln">26 </span>        <span class="name">y</span> <span class="operator">=</span> <span class="name">x</span><span class="operator">*</span><span class="name">x</span><span class="operator">;</span>
<span class="ln">27 </span>        <span class="name">System</span><span class="operator">.</span><span class="name attribute">out</span><span class="operator">.</span><span class="name attribute">println</span><span class="operator">(</span> <span class="literal string">"x*x is "</span> <span class="operator">+</span> <span class="name">y</span> <span class="operator">);</span>
<span class="ln">28 </span>        <span class="name">z</span> <span class="operator">=</span> <span class="name">b</span> <span class="operator">/</span> <span class="literal number integer">2</span><span class="operator">;</span>
<span class="ln">29 </span>        <span class="name">System</span><span class="operator">.</span><span class="name attribute">out</span><span class="operator">.</span><span class="name attribute">println</span><span class="operator">(</span> <span class="literal string">"b/2 is "</span> <span class="operator">+</span> <span class="name">z</span> <span class="operator">);</span>
<span class="ln">30 </span>        <span class="name">System</span><span class="operator">.</span><span class="name attribute">out</span><span class="operator">.</span><span class="name attribute">println</span><span class="operator">();</span>
<span class="ln">31 </span>
<span class="ln">32 </span>        <span class="name">one</span> <span class="operator">=</span> <span class="literal string">"dog"</span><span class="operator">;</span>
<span class="ln">33 </span>        <span class="name">two</span> <span class="operator">=</span> <span class="literal string">"house"</span><span class="operator">;</span>
<span class="ln">34 </span>        <span class="name">both</span> <span class="operator">=</span> <span class="name">one</span> <span class="operator">+</span> <span class="name">two</span><span class="operator">;</span>
<span class="ln">35 </span>        <span class="name">System</span><span class="operator">.</span><span class="name attribute">out</span><span class="operator">.</span><span class="name attribute">println</span><span class="operator">(</span> <span class="name">both</span> <span class="operator">);</span>
<span class="ln">36 </span>    <span class="operator">}</span>
<span class="ln">37 </span><span class="operator">}</span>
</pre>
<div id="what-you-should-see" class="section">
<h1>What You Should See</h1>
<pre class="terminal literal-block">a is 10, b is 27
a+b is 37
a-b is -17
a+b*3 is 91
b/2 is 13
b%10 is 7

x is 1.1
x*x is 1.2100000000000002
b/2 is 13.0

doghouse

</pre>
<p>The plus sign (+) will add two integers or two doubles together, or one integer and one double (in either order). With two Strings (like on line 34) it will concatenate<a id="id1" class="footnote-reference" href="#concat2">[1]</a> the two Strings together.</p>
<p>The minus sign (-) will subtract one number from another. Just like addition, it works with two integers, two doubles, or one integer and one double (in either order).</p>
<p>An asterisk (*) is used to represent multiplication. You can also see on line 17 that Java knows about the correct order of operations. <em>b</em> is multiplied by 3 giving 81 and then <em>a</em> is added.</p>
<p>A slash (/) is used for division. Notice that when an integer is divided by another integer (like on line 19) the result is also an integer and not a double.</p>
<p>The percent sign (%) is used to mean &lsquo;modulus&rsquo;, which is essentially the remainder left over after dividing. On line 21, <em>b</em> is divided by 10 and the remainder (7) is stored into the variable <em>g</em>.</p>
</div>
<div id="common-student-questions" class="section">
<h1>Common Student Questions</h1>
<ul>
<li>
<p class="first">Why is 1.1 times 1.1 equal to 1.2100000000000002 instead of just 1.21?</p>
<blockquote>
<p>Why is 0.333333 + 0.666666 equal to 0.999999 instead of 1.0? Sometimes with math we get repeating decimals, and most computers convert numbers into binary before working with them. It turns out that 1.1 is a repeating decimal in binary.</p>
<p>Remember what I said in the last exercise: the problem with doubles is limited precision. You will mostly be able to ignore that fact in this book, but I would like you to keep in the back of your mind that double variables sometimes give you values that are <em>slightly</em> different than you&rsquo;d expect.</p>
</blockquote>
</li>
</ul>
</div>