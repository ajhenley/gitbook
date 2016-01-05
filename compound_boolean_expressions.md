<!--djw:done but wouldn't hurt to come up with an assignment for this-->
###Compound Boolean Expressions
Sometimes we want to use logic more complicated than just &ldquo;less than&rdquo; or &ldquo;equal to&rdquo;. Project managers are constantly asking for software to be developed. And they want it to be done quickly, for minimal cost and at the highest quality. The rule is: **We can make it fast, cheap or good. Pick two**.

{%ace edit=true, lang='java'%}
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

{%endace%}


For complicated Boolean expressions you can use parentheses to group things, and you use the symbols &amp;&amp; to mean &ldquo;AND&rdquo; and the symbols || to mean &ldquo;OR&rdquo;.


####Truth table for AND:
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

####Truth table for OR:
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
