# For loops

 <h1 class="page-title">For Loops</h1>
  
    <h1>Counting with a For Loop</h1>
<p>As&nbsp;you&nbsp;have&nbsp;seen&nbsp;in&nbsp;previous&nbsp;exercises,&nbsp;while&nbsp;loops&nbsp;and&nbsp;do-while&nbsp;loops&nbsp;can&nbsp;be&nbsp;used&nbsp;to&nbsp;to&nbsp;make&nbsp;something&nbsp;happen&nbsp;more&nbsp;than&nbsp;once</p>
<p>But&nbsp;both&nbsp;kinds&nbsp;of&nbsp;loops&nbsp;are&nbsp;designed&nbsp;to&nbsp;keep&nbsp;going&nbsp;as&nbsp;long&nbsp;as&nbsp;something&nbsp;is&nbsp;true.&nbsp;If&nbsp;we&nbsp;know&nbsp;in&nbsp;advance&nbsp;how&nbsp;many&nbsp;times&nbsp;we&nbsp;want&nbsp;to&nbsp;do&nbsp;something,&nbsp;Java&nbsp;has&nbsp;a&nbsp;special&nbsp;kind&nbsp;of&nbsp;loop&nbsp;designed&nbsp;just&nbsp;for&nbsp;making&nbsp;a&nbsp;variable&nbsp;change&nbsp;values:&nbsp;the&nbsp;for&nbsp;loop.</p>
<pre>&nbsp;1&nbsp;import&nbsp;java.util.Scanner;
&nbsp;2&nbsp;
&nbsp;3&nbsp;public&nbsp;class&nbsp;CountingFor
&nbsp;4&nbsp;{
&nbsp;5&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;public&nbsp;static&nbsp;void&nbsp;main(&nbsp;String[]&nbsp;args&nbsp;)
&nbsp;6&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{
&nbsp;7&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Scanner&nbsp;keyboard&nbsp;=&nbsp;new&nbsp;Scanner(System.in);
&nbsp;8&nbsp;
&nbsp;9&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;int&nbsp;n;
10&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;String&nbsp;message;
11&nbsp;
12&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println(&nbsp;"Type&nbsp;in&nbsp;a&nbsp;message,&nbsp;and&nbsp;I'll&nbsp;display&nbsp;it&nbsp;five&nbsp;
times."&nbsp;);
13&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.print(&nbsp;"Message:&nbsp;"&nbsp;);
14&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;message&nbsp;=&nbsp;keyboard.nextLine();
15&nbsp;
16&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;for&nbsp;(&nbsp;n&nbsp;=&nbsp;1&nbsp;;&nbsp;n&nbsp;&lt;&nbsp;5&nbsp;;&nbsp;n++&nbsp;)
29&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{
30&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;System.out.println(&nbsp;n&nbsp;+&nbsp;".&nbsp;"&nbsp;+&nbsp;message&nbsp;);
31&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
32&nbsp;
33&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
34&nbsp;}
</pre>
<h4>What You Should See</h4>
<pre>Type&nbsp;in&nbsp;a&nbsp;message,&nbsp;and&nbsp;I'll&nbsp;display&nbsp;it&nbsp;five&nbsp;times.
Message:&nbsp;Howdy,&nbsp;y'all!
1.&nbsp;Howdy,&nbsp;y'all!
2.&nbsp;Howdy,&nbsp;y'all!
3.&nbsp;Howdy,&nbsp;y'all!
4.&nbsp;Howdy,&nbsp;y'all!
5.&nbsp;Howdy,&nbsp;y'all!


</pre>
<p>Line&nbsp;16&nbsp;demonstrates&nbsp;a&nbsp;very&nbsp;basic&nbsp;for&nbsp;loop.&nbsp;Every&nbsp;for&nbsp;loop&nbsp;has&nbsp;three&nbsp;parts&nbsp;with&nbsp;semicolons&nbsp;between.</p>
<p>The&nbsp;first&nbsp;part&nbsp;(n=1)&nbsp;only&nbsp;happens&nbsp;once&nbsp;no&nbsp;matter&nbsp;how&nbsp;many&nbsp;times&nbsp;the&nbsp;loop&nbsp;repeats.&nbsp;It&nbsp;happens&nbsp;at&nbsp;the&nbsp;very&nbsp;beginning&nbsp;of&nbsp;the&nbsp;loop&nbsp;and&nbsp;usually&nbsp;sets&nbsp;a&nbsp;starting&nbsp;value&nbsp;for&nbsp;some&nbsp;variable&nbsp;that&nbsp;is&nbsp;going&nbsp;to&nbsp;be&nbsp;used&nbsp;to&nbsp;control&nbsp;the&nbsp;loop.&nbsp;In&nbsp;this&nbsp;case,&nbsp;our&nbsp;“loop&nbsp;control&nbsp;variable”&nbsp;is&nbsp;n&nbsp;and&nbsp;it&nbsp;will&nbsp;start&nbsp;with&nbsp;a&nbsp;value&nbsp;of&nbsp;1.</p>
<p>The&nbsp;second&nbsp;part&nbsp;(n&nbsp;&lt;=&nbsp;5)&nbsp;is&nbsp;a&nbsp;condition,&nbsp;just&nbsp;like&nbsp;the&nbsp;condition&nbsp;of&nbsp;a&nbsp;while&nbsp;or&nbsp;do­while&nbsp;loop.&nbsp;The&nbsp;for loop&nbsp;is&nbsp;a&nbsp;pre-test&nbsp;loop&nbsp;just&nbsp;like&nbsp;a&nbsp;while&nbsp;loop,&nbsp;which&nbsp;means&nbsp;that&nbsp;this&nbsp;condition&nbsp;is&nbsp;tested&nbsp;before&nbsp;the&nbsp;loop&nbsp;starts&nbsp;looping.&nbsp;If&nbsp;the&nbsp;condition&nbsp;is&nbsp;true,&nbsp;the&nbsp;loop&nbsp;body&nbsp;will&nbsp;be&nbsp;executed&nbsp;one&nbsp;time.&nbsp;If&nbsp;the&nbsp;condition&nbsp;is&nbsp;false,&nbsp;the&nbsp;loop&nbsp;body&nbsp;will&nbsp;be&nbsp;skipped&nbsp;and&nbsp;the&nbsp;loop&nbsp;is&nbsp;over.</p>
<p>The&nbsp;third&nbsp;part&nbsp;(n++)&nbsp;runs&nbsp;after&nbsp;each&nbsp;iteration&nbsp;of&nbsp;the&nbsp;loop,&nbsp;just&nbsp;before&nbsp;it&nbsp;checks&nbsp;the&nbsp;condition&nbsp;again.&nbsp;Remember&nbsp;that&nbsp;++&nbsp;adds&nbsp;one&nbsp;to&nbsp;a&nbsp;variable.</p>
<p>So&nbsp;if&nbsp;we&nbsp;unroll&nbsp;this&nbsp;loop,&nbsp;these&nbsp;are&nbsp;the&nbsp;statements&nbsp;that&nbsp;will&nbsp;happen&nbsp;and&nbsp;their&nbsp;order:</p>
<pre>n&nbsp;=&nbsp;1;
//&nbsp;check&nbsp;if&nbsp;(&nbsp;n&nbsp;&lt;=&nbsp;5&nbsp;),&nbsp;which&nbsp;is&nbsp;true
System.out.println(&nbsp;1&nbsp;+&nbsp;"."&nbsp;+&nbsp;message&nbsp;);
n++;&nbsp;//&nbsp;so&nbsp;now&nbsp;n&nbsp;is&nbsp;2
//&nbsp;check&nbsp;if&nbsp;(&nbsp;n&nbsp;&lt;=&nbsp;5&nbsp;),&nbsp;which&nbsp;is&nbsp;true
System.out.println(&nbsp;2&nbsp;+&nbsp;"."&nbsp;+&nbsp;message&nbsp;);
n++;&nbsp;//&nbsp;so&nbsp;now&nbsp;n&nbsp;is&nbsp;3
//&nbsp;check&nbsp;if&nbsp;(&nbsp;n&nbsp;&lt;=&nbsp;5&nbsp;),&nbsp;which&nbsp;is&nbsp;true
System.out.println(&nbsp;3&nbsp;+&nbsp;"."&nbsp;+&nbsp;message&nbsp;);
n++;&nbsp;//&nbsp;so&nbsp;now&nbsp;n&nbsp;is&nbsp;4
//&nbsp;check&nbsp;if&nbsp;(&nbsp;n&nbsp;&lt;=&nbsp;5&nbsp;),&nbsp;which&nbsp;is&nbsp;true
System.out.println(&nbsp;4&nbsp;+&nbsp;"."&nbsp;+&nbsp;message&nbsp;);
n++;&nbsp;//&nbsp;so&nbsp;now&nbsp;n&nbsp;is&nbsp;5
//&nbsp;check&nbsp;if&nbsp;(&nbsp;n&nbsp;&lt;=&nbsp;5&nbsp;),&nbsp;which&nbsp;is&nbsp;true
System.out.println(&nbsp;5&nbsp;+&nbsp;"."&nbsp;+&nbsp;message&nbsp;);
n++;&nbsp;//&nbsp;so&nbsp;now&nbsp;n&nbsp;is&nbsp;6
//&nbsp;check&nbsp;if&nbsp;(&nbsp;n&nbsp;&lt;=&nbsp;6&nbsp;),&nbsp;which&nbsp;is&nbsp;false.&nbsp;The&nbsp;loop&nbsp;stops
</pre>
<p>Notice&nbsp;that&nbsp;the&nbsp;first&nbsp;part&nbsp;only&nbsp;happened&nbsp;once,&nbsp;and&nbsp;that&nbsp;the&nbsp;third&nbsp;part&nbsp;happened&nbsp;exactly&nbsp;as&nbsp;many&nbsp;times&nbsp;as&nbsp;the&nbsp;loop&nbsp;body&nbsp;did.</p>
<p>On&nbsp;line&nbsp;22&nbsp;there&nbsp;is&nbsp;another&nbsp;for&nbsp;loop.&nbsp;The&nbsp;loop&nbsp;control&nbsp;variable&nbsp;is&nbsp;still&nbsp;n.&nbsp;(Notice&nbsp;that&nbsp;the&nbsp;loop&nbsp;control&nbsp;variable&nbsp;appears&nbsp;in&nbsp;all&nbsp;three&nbsp;parts&nbsp;of&nbsp;the&nbsp;loop.&nbsp;This&nbsp;is&nbsp;almost&nbsp;always&nbsp;the&nbsp;case.)</p>
<p>The&nbsp;first&nbsp;part&nbsp;(the&nbsp;“initialization&nbsp;expression”)&nbsp;sets&nbsp;the&nbsp;loop&nbsp;control&nbsp;variable&nbsp;to&nbsp;start&nbsp;at&nbsp;5.&nbsp;Then&nbsp;the&nbsp;second part&nbsp;checks&nbsp;to&nbsp;see&nbsp;if&nbsp;n&nbsp;is&nbsp;less&nbsp;than&nbsp;or&nbsp;equal&nbsp;to&nbsp;50.&nbsp;If&nbsp;so,&nbsp;the&nbsp;body&nbsp;is&nbsp;executed&nbsp;one&nbsp;time&nbsp;and&nbsp;then&nbsp;the&nbsp;third&nbsp;part&nbsp;is&nbsp;executed.&nbsp;The&nbsp;third&nbsp;part&nbsp;adds&nbsp;5&nbsp;to&nbsp;the&nbsp;loop&nbsp;control&nbsp;variable,&nbsp;and&nbsp;then&nbsp;the&nbsp;condition&nbsp;is&nbsp;checked&nbsp;again.&nbsp;If&nbsp;it&nbsp;is&nbsp;still&nbsp;true,&nbsp;the&nbsp;loop&nbsp;repeats.&nbsp;Once&nbsp;it&nbsp;is&nbsp;false,&nbsp;the&nbsp;loop&nbsp;stops.</p>
<p>On&nbsp;line&nbsp;28&nbsp;there&nbsp;is&nbsp;one&nbsp;final&nbsp;for&nbsp;loop.&nbsp;This&nbsp;time&nbsp;the&nbsp;loop&nbsp;control&nbsp;variable&nbsp;starts&nbsp;at&nbsp;3&nbsp;and&nbsp;the&nbsp;loop&nbsp;repeats&nbsp;as&nbsp;long&nbsp;as&nbsp;n&nbsp;is&nbsp;greater&nbsp;than&nbsp;zero.&nbsp;And&nbsp;after&nbsp;each&nbsp;iteration&nbsp;of&nbsp;the&nbsp;loop&nbsp;body&nbsp;the&nbsp;third&nbsp;part&nbsp;(the&nbsp;“update&nbsp;expression”)&nbsp;subtracts 1&nbsp;from&nbsp;the&nbsp;loop&nbsp;control&nbsp;variable.</p>
<p>So&nbsp;when&nbsp;should&nbsp;you&nbsp;use&nbsp;a&nbsp;for&nbsp;loop&nbsp;versus&nbsp;a&nbsp;while&nbsp;loop?</p>
<p>for&nbsp;loops&nbsp;are&nbsp;best&nbsp;when&nbsp;we&nbsp;know&nbsp;in&nbsp;advance&nbsp;how&nbsp;many&nbsp;times&nbsp;we&nbsp;want&nbsp;to&nbsp;do&nbsp;something.</p>
<ul>
<li>Do&nbsp;this&nbsp;ten&nbsp;times.</li>
<li>Do&nbsp;this&nbsp;five&nbsp;times.</li>
<li>Pick&nbsp;a&nbsp;random&nbsp;number,&nbsp;and&nbsp;do&nbsp;it&nbsp;that&nbsp;many&nbsp;times.</li>
<li>Take&nbsp;this&nbsp;list&nbsp;of&nbsp;items,&nbsp;and&nbsp;do&nbsp;it&nbsp;one&nbsp;time&nbsp;for&nbsp;each&nbsp;item&nbsp;in&nbsp;the&nbsp;list.</li>
</ul>
<p>On&nbsp;the&nbsp;other&nbsp;hand,&nbsp;while&nbsp;and&nbsp;do­while&nbsp;loops&nbsp;are&nbsp;best&nbsp;for&nbsp;repeating&nbsp;as&nbsp;long&nbsp;as&nbsp;something&nbsp;is&nbsp;true:</p>
<ul>
<li>Keep&nbsp;going&nbsp;as&nbsp;long&nbsp;as&nbsp;they&nbsp;haven’t&nbsp;guessed&nbsp;it.</li>
<li>Keep&nbsp;going&nbsp;as&nbsp;long&nbsp;as&nbsp;you&nbsp;haven’t&nbsp;got&nbsp;doubles.</li>
<li>Keep&nbsp;going&nbsp;as&nbsp;long&nbsp;as&nbsp;they&nbsp;keep&nbsp;typing&nbsp;in&nbsp;a&nbsp;negative&nbsp;number.</li>
<li>Keep&nbsp;going&nbsp;as&nbsp;long&nbsp;as&nbsp;they&nbsp;haven’t&nbsp;typed&nbsp;in&nbsp;a&nbsp;zero.</li>
</ul>
<h4></h4>
<ol>
<li>Delete&nbsp;the&nbsp;first&nbsp;part&nbsp;(the&nbsp;“initialization&nbsp;expression”)&nbsp;from&nbsp;the&nbsp;third&nbsp;loop.&nbsp;If&nbsp;you&nbsp;remove&nbsp;it&nbsp;correctly,&nbsp;it&nbsp;will&nbsp;still&nbsp;compile.&nbsp;What&nbsp;happens&nbsp;when&nbsp;you&nbsp;run&nbsp;it?</li>
</ol>
  
</div>