# Variables

Programs would be pretty boring if the only thing you could do was print things on the screen. We would like our programs to be interactive.

Interactivity requires several different concepts working together, and explaining them all at once might be confusing. So I am going to cover them one at a time.

First up: variables! If you have ever taken an Algebra class, you are familiar with the concept of variables in mathematics. Programming languages have variables, too, and the basic concept is the same:
<blockquote>&ldquo;A variable is a name that refers to a location that holds a value.&rdquo;</blockquote>
<p>Variables in Java have four major differences from math variables:</p>
* Variable names can be more than one letter long.
* Variables can hold more than just numbers; they can hold words.
* You have to choose what type of values the variable will hold when the variable is first created.
* The value of a variable (but not its type) can change 
throughout the program. The variable score might start out with a value of 0, but by the end of the program, score might hold the value 413500 instead.

<p>Okay, enough discussion. Let&rsquo;s get to the code! I&rsquo;m not going to tell you what the name of the file is supposed to be. You&rsquo;ll have to figure it out for yourself.</p>
<pre class="code java literal-block"><span class="ln"> 1 </span><span class="keyword declaration">public</span> <span class="keyword declaration">class</span> <span class="name class">CreatingVariables</span>
<span class="ln"> 2 </span><span class="operator">{</span>
<span class="ln"> 3 </span>    <span class="keyword declaration">public</span> <span class="keyword declaration">static</span> <span class="keyword type">void</span> <span class="name function">main</span><span class="operator">(</span> <span class="name">String</span><span class="operator">[]</span> <span class="name">args</span> <span class="operator">)</span>
<span class="ln"> 4 </span>    <span class="operator">{</span>
<span class="ln"> 5 </span>        <span class="keyword type">int</span> <span class="name">x</span><span class="operator">,</span> <span class="name">y</span><span class="operator">,</span> <span class="name">age</span><span class="operator">;</span>
<span class="ln"> 6 </span>        <span class="keyword type">double</span> <span class="name">seconds</span><span class="operator">,</span> <span class="name">e</span><span class="operator">,</span> <span class="name">checking</span><span class="operator">;</span>
<span class="ln"> 7 </span>        <span class="name">String</span> <span class="name">firstName</span><span class="operator">,</span> <span class="name">last_name</span><span class="operator">,</span> <span class="name">title</span><span class="operator">;</span>
<span class="ln"> 8 </span>
<span class="ln"> 9 </span>        <span class="name">x</span> <span class="operator">=</span> <span class="literal number integer">10</span><span class="operator">;</span>
<span class="ln">10 </span>        <span class="name">y</span> <span class="operator">=</span> <span class="literal number integer">400</span><span class="operator">;</span>
<span class="ln">11 </span>        <span class="name">age</span> <span class="operator">=</span> <span class="literal number integer">39</span><span class="operator">;</span>
<span class="ln">12 </span>
<span class="ln">13 </span>        <span class="name">seconds</span> <span class="operator">=</span> <span class="literal number float">4.71</span><span class="operator">;</span>
<span class="ln">14 </span>        <span class="name">e</span> <span class="operator">=</span> <span class="literal number float">2.71828182845904523536</span><span class="operator">;</span>
<span class="ln">15 </span>        <span class="name">checking</span> <span class="operator">=</span> <span class="literal number float">1.89</span><span class="operator">;</span>
<span class="ln">16 </span>
<span class="ln">17 </span>        <span class="name">firstName</span> <span class="operator">=</span> <span class="literal string">"Alton"</span><span class="operator">;</span>
<span class="ln">18 </span>        <span class="name">last_name</span> <span class="operator">=</span> <span class="literal string">"Henley"</span><span class="operator">;</span>
<span class="ln">19 </span>        <span class="name">title</span> <span class="operator">=</span> <span class="literal string">"Mr."</span><span class="operator">;</span>
<span class="ln">20 </span>
<span class="ln">21 </span>        <span class="name">System</span><span class="operator">.</span><span class="name attribute">out</span><span class="operator">.</span><span class="name attribute">println</span><span class="operator">(</span> <span class="literal string">"The variable x contains "</span> <span class="operator">+</span> <span class="name">x</span> <span class="operator">);</span>
<span class="ln">22 </span>        <span class="name">System</span><span class="operator">.</span><span class="name attribute">out</span><span class="operator">.</span><span class="name attribute">println</span><span class="operator">(</span> <span class="literal string">"The value "</span> <span class="operator">+</span> <span class="name">y</span> <span class="operator">+</span> <span class="literal string">" is stored in the variable y."</span> <span class="operator">);</span>
<span class="ln">23 </span>        <span class="name">System</span><span class="operator">.</span><span class="name attribute">out</span><span class="operator">.</span><span class="name attribute">println</span><span class="operator">(</span> <span class="literal string">"The experiment completed in "</span> <span class="operator">+</span> <span class="name">seconds</span> <span class="operator">+</span> <span class="literal string">" seconds."</span> <span class="operator">);</span>
<span class="ln">24 </span>        <span class="name">System</span><span class="operator">.</span><span class="name attribute">out</span><span class="operator">.</span><span class="name attribute">println</span><span class="operator">(</span> <span class="literal string">"My favorite irrational number is Euler's constant: "</span> <span class="operator">+</span> <span class="name">e</span> <span class="operator">);</span>
<span class="ln">25 </span>        <span class="name">System</span><span class="operator">.</span><span class="name attribute">out</span><span class="operator">.</span><span class="name attribute">println</span><span class="operator">(</span> <span class="literal string">"Hopefully your balance is more than $"</span> <span class="operator">+</span> <span class="name">checking</span> <span class="operator">+</span> <span class="literal string">"!"</span> <span class="operator">);</span>
<span class="ln">26 </span>        <span class="name">System</span><span class="operator">.</span><span class="name attribute">out</span><span class="operator">.</span><span class="name attribute">println</span><span class="operator">(</span> <span class="literal string">"My full name is "</span> <span class="operator">+</span> <span class="name">title</span> <span class="operator">+</span> <span class="literal string">" "</span> <span class="operator">+</span> <span class="name">firstName</span> <span class="operator">+</span> <span class="name">last_name</span> <span class="operator">);</span>
<span class="ln">27 </span>    <span class="operator">}</span>
<span class="ln">28 </span><span class="operator">}</span>
</pre>
<div id="what-you-should-see" class="section">
<h1>What You Should See</h1>
<pre class="terminal literal-block">The variable x contains 10
The value 400 is stored in the variable y.
The experiment completed in 4.71 seconds.
My favorite irrational number is Euler's constant: 2.718281828459045
Hopefully your balance is more than $1.89!
My full name is Mr. AltonHenley

</pre>
<p>On lines 5 through 7 we declare<a id="id1" class="footnote-reference" href="#declare">[1]</a> nine variables. The first three are named <em>x</em>, <em>y</em>, and <em>age</em>. All three of these variables are &ldquo;integers&rdquo;, which is the type of variable that can hold a value between &plusmn; two billion.</p>
<p>A variable which is an integer could hold the value 10. It could hold the value <span class="pre">-8192</span>. An integer variable can hold 123456789. It could <em>not</em> hold the value 3.14 because that has a fractional part. An integer variable could <em>not</em> hold the value 10000000000 because ten billion is too big.</p>
<p>On line 6 we declare variables named <em>seconds</em>, <em>e</em>, and <em>checking</em>. These three variables are &ldquo;doubles&rdquo;, which is the type of variable that can hold a number that might have a fractional part.</p>
<p>A variable which is a double could hold the value 4.71. It could hold the value <span class="pre">-8192</span>. (It <em>may</em> have a fractional part but doesn&rsquo;t have to.) It can pretty much hold <em>any</em> value between &plusmn; 1.79769 &times; 10<sup>308</sup> and 4.94065 &times; 10<sup>-324</sup>.</p>
<p>However, doubles have limited precision. Notice that on line 14 I store the value 2.71828182845904523536 into the variable named <em>e</em>, but when I print out that value on line 24, only 2.718281828459045 comes out. Doubles do not have enough significant figures to hold the value 2.71828182845904523536 precisely. Integers have perfect precision, but can only hold whole numbers and can&rsquo;t hold huge huge values.</p>
<p>The last type of variable we are going to look at in this exercise is the String. On line 7 we declare three String variables: <em>firstName</em>, <em>last_name</em> and <em>title</em>. String variables can hold words and phrases; the name is short for &ldquo;string of characters&rdquo;.</p>
<p>On lines 9 through 11 we initialize<a id="id2" class="footnote-reference" href="#initialize">[2]</a> the three integer values. The value 10 is stored into <em>x</em>. Before this point, the variable <em>x</em> exists, but its value is undefined. 400 is stored into <em>y</em> and 39 is stored into the variable <em>age</em>.</p>
<p>Lines 13 through 15 give initial values to the three double variables, and lines 17 through 19 initialize the three String variables. Then lines 21 through 26 display the values of those variables on the screen. Notice that the variable names are not surrounded by quotes.</p>
<p>I know that it doesn&rsquo;t make sense to use variables for a program like this, but soon everything will become clear.</p>
</div>