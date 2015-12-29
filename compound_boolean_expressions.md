###Compound Boolean Expressions


<p>Sometimes we want to use logic more complicated than just &ldquo;less than&rdquo; or &ldquo;equal to&rdquo;. Project managers are constantly asking for software to be developed. And they want it to be done quickly, for minimal cost and at the highest quality. The rule is: **We can make it fast, cheap or good. Pick two**.

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


So we can see that for complicated Boolean expressions you can use parentheses to group things, and you use the symbols &amp;&amp; to mean &ldquo;AND&rdquo; and the symbols || to mean &ldquo;OR&rdquo;.

<blockquote>
Java syntax is modeled after C++&rsquo;s syntax, which was basically copied from C&rsquo;s syntax, and that was modified from B&rsquo;s syntax, which was invented by Dennis Ritchie and Ken Thompson.</p>
<p>The programming language <em>B</em> used &amp; to mean &ldquo;AND&rdquo; and | for &ldquo;OR&rdquo;, but they were &ldquo;bitwise&rdquo;: they only worked on two integers and they would walk one bit at a time down the integers doing a bitwise AND or OR on each pair of bits, putting a 1 or 0 in the output for each comparison. (| was probably used because it was mathematical-looking and was a key on the keyboards of the PDP-7 computer that <em>B</em> was originally developed for.)</p>
<p>When Ken and Dennis started developing the programming language <em>C</em> to replace <em>B</em>, they decided there was a need for a <em>logical</em> &ldquo;AND&rdquo; and &ldquo;OR&rdquo;, and the one-symbol-long things were already taken, so they used two ampersands to represent logical &ldquo;AND&rdquo; and two vertical bars or &ldquo;pipes&rdquo; to represent logical &ldquo;OR&rdquo;.</p>
</blockquote>


####truth table for AND:
<table border="1">
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


<table border="1"><colgroup> <col width="28%" /> <col width="28%" /> <col width="44%" /> </colgroup>
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
