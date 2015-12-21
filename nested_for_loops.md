# Nested for loops

create a nested loop to print an outline format 
the outer loop would contain numbers the inner loop would contain letters
create nested loop to multiplication table



    <h1>Nested&nbsp;For&nbsp;Loops</h1>
<p>In&nbsp;programming,&nbsp;the&nbsp;term&nbsp;“nested”&nbsp;usually&nbsp;means&nbsp;to&nbsp;put&nbsp;something&nbsp;inside&nbsp;the&nbsp;same&nbsp;thing.&nbsp; “Nested&nbsp;loops”&nbsp;would&nbsp;be&nbsp;two&nbsp;loops&nbsp;with&nbsp;one&nbsp;inside&nbsp;the&nbsp;other&nbsp;one.&nbsp;If&nbsp;you&nbsp;do&nbsp;it&nbsp;right,&nbsp;then&nbsp; means&nbsp;the&nbsp;inner&nbsp;loop&nbsp;will&nbsp;repeat&nbsp;all&nbsp;its&nbsp;iterations&nbsp;every&nbsp;time&nbsp;the&nbsp;outer&nbsp;loop&nbsp;does&nbsp;one&nbsp;more&nbsp; iteration.</p>
<pre>&nbsp;1&nbsp;public&nbsp;class&nbsp;NestingLoops
&nbsp;2&nbsp;{
&nbsp;3&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;public&nbsp;static&nbsp;void&nbsp;main(&nbsp;String[]&nbsp;args&nbsp;)
&nbsp;4&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{
&nbsp;5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;//&nbsp;this&nbsp;is&nbsp;#1&nbsp;­&nbsp;I'll&nbsp;call&nbsp;it&nbsp;"CN"
&nbsp;6&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;for&nbsp;(&nbsp;char&nbsp;c='A';&nbsp;c&nbsp;&lt;=&nbsp;'E';&nbsp;c++&nbsp;)
&nbsp;7&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{
&nbsp;8&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;for&nbsp;(&nbsp;int&nbsp;n=1;&nbsp;n&nbsp;&lt;=&nbsp;3;&nbsp;n++&nbsp;)
&nbsp;9&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{
10&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println(&nbsp;c&nbsp;+&nbsp;"&nbsp;"&nbsp;+&nbsp;n&nbsp;);
11&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
12&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
13&nbsp;
14&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println("\n");
15&nbsp;
16&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;//&nbsp;this&nbsp;is&nbsp;#2&nbsp;­&nbsp;I'll&nbsp;call&nbsp;it&nbsp;"AB"
17&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;for&nbsp;(&nbsp;int&nbsp;a=1;&nbsp;a&nbsp;&lt;=&nbsp;3;&nbsp;a++&nbsp;)
18&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{
19&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;for&nbsp;(&nbsp;int&nbsp;b=1;&nbsp;b&nbsp;&lt;=&nbsp;3;&nbsp;b++&nbsp;)
20&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{
21&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.print(&nbsp;"("&nbsp;+&nbsp;a&nbsp;+&nbsp;","&nbsp;+&nbsp;b&nbsp;+&nbsp;")&nbsp;"&nbsp;);
22&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
23&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;//&nbsp;*&nbsp;You&nbsp;will&nbsp;add&nbsp;a&nbsp;line&nbsp;of&nbsp;code&nbsp;here.
24&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
25&nbsp;
26&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println("\n");
27&nbsp;
28&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
29&nbsp;}
</pre>
<h4>What You Should See</h4>
<pre>A&nbsp;1
A&nbsp;2
A&nbsp;3
B&nbsp;1
B&nbsp;2
B&nbsp;3
C&nbsp;1
C&nbsp;2
C&nbsp;3
D&nbsp;1
D&nbsp;2
D&nbsp;3
E&nbsp;1
E&nbsp;2
E&nbsp;3
(1,1)&nbsp;(1,2)&nbsp;(1,3)&nbsp;(2,1)&nbsp;(2,2)&nbsp;(2,3)&nbsp;(3,1)&nbsp;(3,2)&nbsp;(3,3)&nbsp;
</pre>
<h4>Study&nbsp;Drills</h4>
<ol>
<li>Look&nbsp;at&nbsp;the&nbsp;first&nbsp;set&nbsp;of&nbsp;nested&nbsp;loops&nbsp;(“CN”).&nbsp;Which&nbsp;variable&nbsp;changes&nbsp;faster?&nbsp;Is&nbsp;it&nbsp;the&nbsp;variable&nbsp;controlled&nbsp;by&nbsp;the&nbsp;outer&nbsp;loop&nbsp;(c)&nbsp;or&nbsp;the&nbsp;variable&nbsp;controlled&nbsp;by&nbsp;the&nbsp;inner&nbsp;loop&nbsp;(n)?</li>
<li>Change&nbsp;the&nbsp;order&nbsp;of&nbsp;the&nbsp;loops&nbsp;so&nbsp;that&nbsp;the&nbsp;“c”&nbsp;loop&nbsp;is&nbsp;on&nbsp;the&nbsp;inside&nbsp;and&nbsp;the&nbsp;“n”&nbsp;loop&nbsp;is&nbsp;on&nbsp;the&nbsp;outside.&nbsp;How&nbsp;does&nbsp;the&nbsp;output&nbsp;change?</li>
<li>Look&nbsp;at&nbsp;the&nbsp;second&nbsp;set&nbsp;of&nbsp;nested&nbsp;loops&nbsp;(“AB”).&nbsp;Change&nbsp;the&nbsp;print()&nbsp;statement&nbsp;to&nbsp;println(). How&nbsp;does&nbsp;the&nbsp;output&nbsp;change?&nbsp;(Then&nbsp;change&nbsp;it&nbsp;back&nbsp;to&nbsp;print().)</li>
<li>Add&nbsp;a&nbsp;System.out.println()&nbsp;statement&nbsp;after&nbsp;the&nbsp;close&nbsp;brace&nbsp;of&nbsp;the&nbsp;inner&nbsp;loop&nbsp;(the&nbsp;“b”&nbsp; loop),&nbsp;but&nbsp;still&nbsp;inside&nbsp;the&nbsp;outer&nbsp;loop.&nbsp;How&nbsp;does&nbsp;the&nbsp;output&nbsp;change?</li>
</ol>
  
</div>