# Git Walkthrough

<h3>Walk-through Git</h3>
<p>For this walk-through, you'll want to open the Git shell. You can type the commands on the left and view the explanation on the right.</p>
<table style="margin-left: auto; margin-right: auto;" border="1">
<tbody>
<tr>
<td width="40%">
<p><strong>Command</strong></p>
</td>
<td width="60%">
<p><strong>Explanation</strong></p>
</td>
</tr>
<tr>
<td width="394">
<p>git help</p>
</td>
<td width="365">
<p>The only command you can't forget is help. This will help you find the other commands.</p>
</td>
</tr>
<tr>
<td width="394">
<p>echo # Products &gt;&gt; README.md</p>
</td>
<td width="365">
<p>The first commit can be a README file with as little as one line summary of the project, or enough information about the project's first milestone. The broad topics can also include:<br /> &nbsp;- Introduction<br /> - Project description<br /> - Project structure<br /> - Coding conventions</p>
</td>
</tr>
<tr>
<td width="394">
<p>git init</p>
</td>
<td width="365">
<p>The git init command creates a new Git repository. It can be used to convert an existing, un-versioned project to a Git repository or initialize a new empty repository. This is the first command you&rsquo;ll run in a new project.<br /> <br /> git init creates a .git subdirectory in your project directory which all of the information git needs for your repository. The rest of an existing project is unchanged.</p>
</td>
</tr>
<tr>
<td width="394">
<p>git add README.md</p>
</td>
<td width="365">
<p>&nbsp;Adds the README file to the index</p>
</td>
</tr>
<tr>
<td width="394">
<p>git commit -m "first commit"</p>
</td>
<td width="365">
<p>The first commit is usually called initial commit or First commit or something similar depending on your preferences. I prefer to get this out of the way and commit before adding many files. From then on I only work from a branch</p>
</td>
</tr>
<tr>
<td width="394">
<p>git remote add origin https://github.com/dave45678/Products.git</p>
</td>
<td width="365">
<p>git remote is used to add a new remote section called origin to our configuration. You can view he config file on windows using the type command. On unix this command is called cat.</p>
</td>
</tr>
<tr>
<td width="394">
<p>type .git/config</p>
</td>
<td width="365">
<p>The name origin is not special or unique. It's just the name that, by convention,&nbsp; refers to the basis repository.</p>
</td>
</tr>
<tr>
<td width="394">
<p>git push -u origin master</p>
</td>
<td width="365">
<p>Any change that we had committed was local to our repository. Those changes don't exist on GitHub yet. You push your changes to GitHub with the push command. Here we're pushing to origin from master.</p>
</td>
</tr>
<tr>
<td width="394">
<p>git status</p>
</td>
<td width="365">
<p>status will show us the state of your index. It will show which files are presently staged.</p>
</td>
</tr>
<tr>
<td width="394">
<p>git branch new_feature</p>
</td>
<td width="365">
<p>Now we add a branch from which to work. A branch is a good way to isolate development of a particular feature. Many developers build their &nbsp;software one feature at a time. Test it. Make sure it works. Then merge the branch back into master and complete the process again.&nbsp;</p>
</td>
</tr>
<tr>
<td width="394">
<p>git checkout new_feature</p>
</td>
<td width="365">
<p>this is how you switch to the new_feature branch</p>
</td>
</tr>
<tr>
<td width="394">
<p>git branch</p>
</td>
<td width="365">
<p>this is how you &nbsp;view the local branches and note the one you&rsquo;re on. In a little while you'll merge your new_feature branch and delete it.</p>
</td>
</tr>
<tr>
<td width="394">
<p>git status</p>
</td>
<td width="365">
<p>status tells you the state of the index</p>
</td>
</tr>
<tr>
<td width="394">
<p>"this is my shirts file"&gt;&gt;shirts.txt</p>
</td>
<td width="365">
<p>create a new file for shirts</p>
</td>
</tr>
<tr>
<td width="394">
<p>git add shirts.txt</p>
</td>
<td width="365">
<p>add that to the index</p>
</td>
</tr>
<tr>
<td width="394">
<p>git status</p>
</td>
<td width="365">
<p>And see what happened</p>
</td>
</tr>
<tr>
<td width="394">
<p>git commit -m "Add shirts to the product line"</p>
</td>
<td width="365">
<p>now commit the shirts to the product line.</p>
</td>
</tr>
<tr>
<td width="394">
<p>"this is the pants file"&gt;&gt;pants.txt</p>
</td>
<td width="365">
<p>Add some pants</p>
</td>
</tr>
<tr>
<td width="394">
<p>"this is the shoes file"&gt;&gt;shoes.txt</p>
</td>
<td width="365">
<p>And some shoes</p>
</td>
</tr>
<tr>
<td width="394">
<p>"this is the ties file"&gt;&gt;ties.txt</p>
</td>
<td width="365">
<p>And some ties</p>
</td>
</tr>
<tr>
<td width="394">
<p>mkdir outerwear</p>
</td>
<td width="365">
<p>You want to add jackets, too. But I want to show you that you can work from sub-directories as well. Git will track all that. So, create a directory for outerwear and put the jackets in it.</p>
</td>
</tr>
<tr>
<td width="394">
<p>"this is the jackets.txt"&gt;&gt;outerwear/jackets.txt</p>
</td>
<td width="365">
<p>Next add the jackets to the outerwear directory</p>
</td>
</tr>
<tr>
<td width="394">
<p>git add *.txt</p>
</td>
<td width="365">
<p>git add can add everything. It will find it all - even the sub-directory.</p>
</td>
</tr>
<tr>
<td width="394">
<p>git commit -m "Add all the product text files"</p>
</td>
<td width="365">
<p>commit the staged changes&nbsp; to the project repository.</p>
</td>
</tr>
<tr>
<td width="394">
<p>git log</p>
</td>
<td width="365">
<p>git log shows the history of commits. It shows the history based on the current branch, unless you specify otherwise</p>
</td>
</tr>
<tr>
<td width="394">
<p>git log master</p>
</td>
<td width="365">
<p>This is Git log showing the history of the master branch. Git log has a number of other features as well.</p>
</td>
</tr>
<tr>
<td width="394">
<p>git checkout master</p>
</td>
<td width="365">
<p>Switch back to the master branch.</p>
</td>
</tr>
<tr>
<td width="394">
<p>git status</p>
</td>
<td width="365">
<p>Use status to see what's going on. None of the other files from new_feature exist on master!</p>
</td>
</tr>
<tr>
<td width="394">
<p>git ls-files</p>
</td>
<td width="365">
<p>In the directory but it's part of the new_feature branch, not master.</p>
</td>
</tr>
<tr>
<td width="394">
<p>git merge new_feature</p>
</td>
<td width="365">
<p>merge the new_feature branch to the current branch, master.</p>
</td>
</tr>
<tr>
<td width="394">
<p>git branch -d new_feature</p>
</td>
<td width="365">
<p>Next delete the new_feature branch. You&rsquo;re done with that for now.</p>
</td>
</tr>
<tr>
<td width="394">
<p>git branch</p>
</td>
<td width="365">
<p>List the branches&hellip; no more new_feature.</p>
</td>
</tr>
<tr>
<td width="394">
<p>git push</p>
</td>
<td width="365">
<p>Push your repository up to GitHub. If you're working with a team you would pull before you push so you could get their changes.</p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>