# Comments

<h3>Comments and Slashes</h3>
<p>Comments are very important in your programs. They are used to tell you what something does in English, and they also are used to disable parts of your program if you need to remove them temporarily. Here's how you use comments in Java:</p>
<pre><strong class="k">public</strong> <strong class="k">class</strong> CommentsAndSlashes
<strong class="b">{</strong>
    <strong class="k">public static void</strong> main<strong class="b">(</strong> <strong class="O">String</strong><strong class="b">[]</strong> args <strong class="b">)</strong>
    <strong class="b">{</strong>
        <strong class="c">// A comment, this is so you can read your program later.</strong>
        <strong class="c">// Anything after the // is ignored by Java.</strong>

        <strong class="O">System</strong>.out.println<strong class="b">(</strong> <strong class="s">"I could have code like this."</strong> <strong class="b">)</strong>; <strong class="c">// and the comment after is ignored.</strong>

        <strong class="c">// You can also use a comment to "disable" or comment out a piece of code:</strong>
        <strong class="c">// System.out.println("This won't run.");</strong>

        <strong class="O">System</strong>.out.println<strong class="b">(</strong> <strong class="s">"This will run."</strong> <strong class="b">)</strong>;
    <strong class="b">}</strong>
<strong class="b">}</strong>
</pre>
<p>From now on, I'm going to write code like this. It is important for you to understand that everything does not have to be literal. Your screen and program may visually look different, but what's important is the text you type into the file you're writing in your text editor. In fact, I could work with any text editor and the results would be the same.</p>
<h2>What You Should See</h2>
<pre class="DOSBOX">I could have code like this.
This will run.
</pre>
<h2>What You Should Do on Your Own</h2>
<p>Assignments turned in <em>without</em> these things will not receive any points. For this exercise, try these things.</p>
<ol>
<li>Were you right about what the two slashes ('//') signify? Answer in a comment at the top of the file (above the 'public class' line).</li>
<li>Add another comment at the <em>very</em> top of the file (above your answer to the previous question) with your name and today's date.</li>
<li>* Insert a multiline comment. Do you know how to do that? Why not?</li>
</ol>