###Compound Boolean Expressions


<p>Sometimes we want to use logic more complicated than just &ldquo;less than&rdquo; or &ldquo;equal to&rdquo;. Imagine a grandmother who will only approve you dating her grandchild if you are older than 25 <em>and</em> younger than 40 <em>and</em> either rich or really good looking. If that grandmother was a programmer and could convince applicants to answer honestly, her program might look a bit like this:</p>

```java
 import java.util.Scanner;

public class ProjectManagerDecisionMaker {

	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);
		boolean bFast = false;
		boolean bCheap = false;
		boolean bGood = false;
		
		System.out.print("Do you want it fast? (y/n) ");
		String fast  = scan.nextLine();
		if (fast.equals("y")){
			bFast = true;
		}
		
		System.out.print("Do you want it cheap? (y/n) ");
	    String cheap = scan.nextLine();
	    if (cheap.equals("y")){
			bCheap = true;
		}
	    
	    System.out.print("Do you want it to be good? (y/n) ");
	    String good = scan.nextLine();
	    if (good.equals("y")){
			bGood = true;
		}
	    
	    if (bFast != true && bCheap == true && bGood == true)
	    	System.out.println("OK, we'll make it cheap and good. But it will take a while.");
	    else if (bFast == true && bCheap !=true && bGood == true)
	    	System.out.println("OK, we'll make it good and have it to you quickly. But it will cost you!");
	    else if (bFast == true && bCheap == true && bGood != true)
	    	System.out.println("Ok, it will be done right away and it won't cost you much but it won't be very good!" );
	    else
	    	System.out.println("Sorry, you can only have two.");
		
	}

}

 ```


<div id="what-you-should-see" class="section">
<h1>What You Should See</h1>
<pre class="terminal literal-block">Enter your age: 39
Enter your yearly income: 49000
How attractive are you, on a scale from 0.0 to 10.0? 7.5
You are allowed to date my grandchild: false
</pre>
<p>So we can see that for complicated Boolean expressions you can use parentheses to group things, and you use the symbols &amp;&amp; to mean &ldquo;AND&rdquo; and the symbols || to mean &ldquo;OR&rdquo;.</p>
<p>I know what you are thinking: using &amp; (an &ldquo;ampersand&rdquo; or &ldquo;and sign&rdquo;) to mean &ldquo;AND&rdquo; makes a little sense, but why two of them? And whose idea was it to use || (&ldquo;pipe pipe&rdquo;) to mean &ldquo;OR&rdquo;?!?</p>
<blockquote>
<p>Well, Ken Thompson&rsquo;s idea, probably. Java syntax is modeled after C++&rsquo;s syntax, which was basically copied from C&rsquo;s syntax, and that was modified from B&rsquo;s syntax, which was invented by Dennis Ritchie and Ken Thompson.</p>
<p>The programming language <em>B</em> used &amp; to mean &ldquo;AND&rdquo; and | for &ldquo;OR&rdquo;, but they were &ldquo;bitwise&rdquo;: they only worked on two integers and they would walk one bit at a time down the integers doing a bitwise AND or OR on each pair of bits, putting a 1 or 0 in the output for each comparison. (| was probably used because it was mathematical-looking and was a key on the keyboards of the PDP-7 computer that <em>B</em> was originally developed for.)</p>
<p>When Ken and Dennis started developing the programming language <em>C</em> to replace <em>B</em>, they decided there was a need for a <em>logical</em> &ldquo;AND&rdquo; and &ldquo;OR&rdquo;, and the one-symbol-long things were already taken, so they used two ampersands to represent logical &ldquo;AND&rdquo; and two vertical bars or &ldquo;pipes&rdquo; to represent logical &ldquo;OR&rdquo;. Whew.</p>
</blockquote>
<p>Fortunately for you, you don&rsquo;t need to know any of that. You just need to remember what to type and get it right.</p>
<p>This next little bit is going to be a little bit weird, because I&rsquo;m going to show you the &ldquo;truth tables&rdquo; for AND and OR, and you&rsquo;ll have to think of &ldquo;AND&rdquo; as an <em>operation</em> that is being performed on two values instead of a conjunction.</p>
<p>Here is the truth table for AND:</p>
<table class="docutils" border="1"><colgroup> <col width="28%" /> <col width="28%" /> <col width="44%" /> </colgroup>
<thead>
<tr>
<th class="head" colspan="2">Inputs</th>
<th class="head">Output(s)</th>
</tr>
<tr>
<th class="head">A</th>
<th class="head">B</th>
<th class="head">A &amp;&amp; B</th>
</tr>
</thead>
<tbody>
<tr>
<td>true</td>
<td>true</td>
<td>true</td>
</tr>
<tr>
<td>true</td>
<td>false</td>
<td>false</td>
</tr>
<tr>
<td>false</td>
<td>true</td>
<td>false</td>
</tr>
<tr>
<td>false</td>
<td>false</td>
<td>false</td>
</tr>
</tbody>
</table>
<p>You read the tables this way: let&rsquo;s pretend that our shallow grandmother has decided that she will only go on a cruise if it is cheap AND the alcohol is included in the price. So we will pretend that statement A is &ldquo;the cruise is cheap&rdquo; and statement B is &ldquo;the alcohol is included&rdquo;. Each row in the table is a possible cruise line.</p>
<p>Row 1 is a cruise where both statements are true. Will grandmother be excited about cruise #1? Yes! &ldquo;Cruise is cheap&rdquo; is true and &ldquo;alcohol is included&rdquo; is true, so &ldquo;grandmother will go&rdquo; (A &amp;&amp; B) is also true.</p>
<p>Cruise #2 is cheap, but the alcohol is <em>not</em> included (statement B is false). So grandmother isn&rsquo;t interested: (A &amp;&amp; B) is false when A is true and B is false.</p>
<p>Clear? Now here is the truth table for OR:</p>
<table class="docutils" border="1"><colgroup> <col width="28%" /> <col width="28%" /> <col width="44%" /> </colgroup>
<thead>
<tr>
<th class="head" colspan="2">Inputs</th>
<th class="head">Output(s)</th>
</tr>
<tr>
<th class="head">A</th>
<th class="head">B</th>
<th class="head">A || B</th>
</tr>
</thead>
<tbody>
<tr>
<td>true</td>
<td>true</td>
<td>true</td>
</tr>
<tr>
<td>true</td>
<td>false</td>
<td>true</td>
</tr>
<tr>
<td>false</td>
<td>true</td>
<td>true</td>
</tr>
<tr>
<td>false</td>
<td>false</td>
<td>false</td>
</tr>
</tbody>
</table>
<p>Let&rsquo;s say that grandmother will buy a certain used car if it is really cool-looking OR if it gets great gas mileage. Statement A is &ldquo;car is cool looking&rdquo;, B is &ldquo;good miles per gallon&rdquo; and the result, A OR B, determines if it is a car grandmother would want.</p>
<p>Car #1 is awesome-looking and it also goes a long way on a tank of gas. Is grandmother interested? Heck, yes! We can say that the value true ORed with the value true gives a result of true.</p>
<p>In fact, the only car grandmother won&rsquo;t like is when both are false. An expression involving OR is only false if BOTH of its components are false.</p>
</div>
<div id="study-drills" class="section">
<h1>Study Drills</h1>
<ol class="arabic simple">
<li>Did you know that Java has bitwise operators, too? Investigate how numbers are represented in binary and see if you can figure out why the following code sets <em>x</em> to the value 7 and sets <em>y</em> to the value 1.</li>
</ol>
<pre class="code java literal-block"><span class="keyword type">int</span> <span class="name">x</span> <span class="operator">=</span> <span class="literal number integer">3</span> <span class="operator">|</span> <span class="literal number integer">5</span><span class="operator">;</span>
<span class="keyword type">int</span> <span class="name">y</span> <span class="operator">=</span> <span class="literal number integer">3</span> <span class="operator">&amp;</span> <span class="literal number integer">5</span><span class="operator">;</span>
</pre>
</div>