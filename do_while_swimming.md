The while loop is good when you don't know how many times a block of code or statement should repeat and you want to continue as long as some condition it true. It looks like this:
```java
while (expression) {
 // do you thing as long as the expression is true
}
```
The while loop will never run if the expression isn't true. So if you're reading from a file while the file is open and the file isn't open then the loop won't run. So there are lots of times when the while loop may not even run.
```java
bool run = false;
while (run){
    //this code would never run
}
```

The do-while loop is similar to the while loop except the expression isn't evaluated until the loop has run at least once.
```java
bool run = false;
do {
    //this code would run once but that's it.
}while (run);
```



###Do while swimming

So far you have only worked with one type of loop: the <code class="k">while</code> loop. But there is another type: the "do-while" loop.</p>
<p>The do-while loop works <em>almost</em> exactly like a <code class="k">while</code> loop. In fact, most of the time they are equivalent. Examine the program below to see if you can figure out the tiny difference.</p>
<p>File:&nbsp;<span class="instructure_file_link_holder link_holder"><a class="" title="DoWhileSwimming.java" href="https://canvas.instructure.com/courses/970783/files/36794442/download?wrap=1" data-api-endpoint="https://canvas.instructure.com/api/v1/courses/970783/files/36794442" data-api-returntype="File">DoWhileSwimming.java</a><a href="https://canvas.instructure.com/courses/970783/files/36794442/download?wrap=1" target="_blank" title="View in a new window" style="padding-left: 5px;"><img src="./Do While Swimming_ Java - Soup to Web - September Cohort_files/popout.png" alt="View in a new window"></a></span></p>
<pre class="CODE"><strong class="k">import</strong> java.util.<strong class="O">Scanner</strong>;

<strong class="k">public</strong> <strong class="k">class</strong> DoWhileSwimming
<strong class="b">{</strong>
    <strong class="k">public static void</strong> main<strong class="b">(</strong> <strong class="O">String</strong><strong class="b">[]</strong> args <strong class="b">)</strong> throws <strong class="O">Exception</strong>
    <strong class="b">{</strong>
        <strong class="O">Scanner</strong> keyboard = <strong class="k">new</strong> <strong class="O">Scanner</strong><strong class="b">(</strong><strong class="O">System</strong>.in<strong class="b">)</strong>;

        <strong class="O">String</strong> swimmer1 = <strong class="s">"GALLANT"</strong>;
        <strong class="O">String</strong> swimmer2 = <strong class="s">"GOOFUS "</strong>;

        <strong class="k">double</strong> minimumTemperature = 79.0; <strong class="c">// degrees Fahrenheit</strong>
        <strong class="k">double</strong> currentTemperature;
        <strong class="k">double</strong> savedTemperature;
        <strong class="k">int</strong> swimTime;

        <strong class="O">System</strong>.out.print<strong class="b">(</strong><strong class="s">"What is the current water temperature? "</strong><strong class="b">)</strong>;
        currentTemperature = keyboard.next<strong class="O">Double</strong><strong class="b"><strong class="b">(</strong><strong class="b">)</strong></strong>;
        savedTemperature = currentTemperature; <strong class="c">// saves a copy of this value so we can get it back later.</strong>

        <strong class="O">System</strong>.out.println<strong class="b">(</strong> <strong class="s">"\nOkay, so the current water temperature is "</strong> + currentTemperature + <strong class="s">"F."</strong> <strong class="b">)</strong>;
        <strong class="O">System</strong>.out.println<strong class="b">(</strong> swimmer1 + <strong class="s">" approaches the lake...."</strong> <strong class="b">)</strong>;

        swimTime = 0;
        <strong class="k">while</strong> <strong class="b">(</strong> currentTemperature &gt;= minimumTemperature <strong class="b">)</strong>
        <strong class="b">{</strong>
            <strong class="O">System</strong>.out.print<strong class="b">(</strong> <strong class="s">"\t"</strong> + swimmer1 + <strong class="s">" swims <strong class="k">for</strong> a bit."</strong> <strong class="b">)</strong>;
            swimTime++;
            <strong class="O">System</strong>.out.println<strong class="b">(</strong> <strong class="s">" Swim time: "</strong> + swimTime + <strong class="s">" min."</strong> <strong class="b">)</strong>;
            Thread.sleep<strong class="b">(</strong>600<strong class="b">)</strong>; <strong class="c">// pauses for 600 milliseconds</strong>
            currentTemperature -= 0.5; <strong class="c">// subtracts 1/2 a degree from the water temperature</strong>
            <strong class="O">System</strong>.out.println<strong class="b">(</strong> <strong class="s">"\tThe current water temperature is now "</strong> + currentTemperature + <strong class="s">"F."</strong> <strong class="b">)</strong>;
        <strong class="b">}</strong>

        <strong class="O">System</strong>.out.println<strong class="b">(</strong> swimmer1 + <strong class="s">" stops swimming. Total swim time: "</strong> + swimTime + <strong class="s">" min."</strong> <strong class="b">)</strong>;

        currentTemperature = savedTemperature; <strong class="c">// restores original water temperature</strong>

        <strong class="O">System</strong>.out.println<strong class="b">(</strong> <strong class="s">"\nOkay, so the current water temperature is "</strong> + currentTemperature + <strong class="s">"F."</strong> <strong class="b">)</strong>;
        <strong class="O">System</strong>.out.println<strong class="b">(</strong> swimmer2 + <strong class="s">" approaches the lake...."</strong> <strong class="b">)</strong>;

        swimTime = 0;
        <strong class="k">do</strong>
        <strong class="b">{</strong>
            <strong class="O">System</strong>.out.print<strong class="b">(</strong> <strong class="s">"\t"</strong> + swimmer2 + <strong class="s">" swims <strong class="k">for</strong> a bit."</strong> <strong class="b">)</strong>;
            swimTime++;
            <strong class="O">System</strong>.out.println<strong class="b">(</strong> <strong class="s">" Swim time: "</strong> + swimTime + <strong class="s">" min."</strong> <strong class="b">)</strong>;
            Thread.sleep<strong class="b">(</strong>600<strong class="b">)</strong>;
            currentTemperature -= 0.5;
            <strong class="O">System</strong>.out.println<strong class="b">(</strong> <strong class="s">"\tThe current water temperature is now "</strong> + currentTemperature + <strong class="s">"F."</strong> <strong class="b">)</strong>;

        <strong class="b">}</strong> <strong class="k">while</strong> <strong class="b">(</strong> currentTemperature &gt;= minimumTemperature <strong class="b">)</strong>;

        <strong class="O">System</strong>.out.println<strong class="b">(</strong> swimmer2 + <strong class="s">" stops swimming. Total swim time: "</strong> + swimTime + <strong class="s">" min."</strong> <strong class="b">)</strong>;
    <strong class="b">}</strong>
<strong class="b">}</strong>
</pre>
<h2>What You Should See</h2>
<p>Goofus and Gallant are both going swimming. They hate to swim in cold water; once the water temperature drops below 79°F, they stop.</p>
<p>Run the program, and type in 80.5 for the water temperature.</p>
<pre class="DOSBOX">What is the current water temperature? 80.5

Okay, so the current water temperature is 80.5F.
GALLANT approaches the lake....
        GALLANT swims for a bit. Swim time: 1 min.
        The current water temperature is now 80.0F.
        GALLANT swims for a bit. Swim time: 2 min.
        The current water temperature is now 79.5F.
        GALLANT swims for a bit. Swim time: 3 min.
        The current water temperature is now 79.0F.
        GALLANT swims for a bit. Swim time: 4 min.
        The current water temperature is now 78.5F.
GALLANT stops swimming. Total swim time: 4 min.

Okay, so the current water temperature is 80.5F.
GOOFUS  approaches the lake....
        GOOFUS  swims for a bit. Swim time: 1 min.
        The current water temperature is now 80.0F.
        GOOFUS  swims for a bit. Swim time: 2 min.
        The current water temperature is now 79.5F.
        GOOFUS  swims for a bit. Swim time: 3 min.
        The current water temperature is now 79.0F.
        GOOFUS  swims for a bit. Swim time: 4 min.
        The current water temperature is now 78.5F.
GOOFUS  stops swimming. Total swim time: 4 min.
</pre>
<h2>What You Should Do on Your Own</h2>
<p>Assignments turned in <em>without</em> these things will receive no credit.</p>
<ol>
<li>Run the program, and type in 80.5 for the current water temperature. Do Goofus and Gallant swim for the same amount of time? Put your answer in a comment.</li>
<li>Run the program again, but this time enter 78 for the starting temperature. What changes?</li>
<li>Does Gallant check the water temperature first, or does he just dive right in?</li>
<li>What about Goofus? Does he check the water temperature first or just dive in?</li>
<li>What is the difference between a <code class="k">while</code> loop and a "do-while" loop?</li>
<li>One of these loops is sometimes called a "pre-test loop", and the other is called a "post-test loop". Which one is which?</li>
</ol>
  
</div>