# Sales Tax Calculator

<p>Create &nbsp;Sales Tax Calculator using JavaScript</p>
<p>The $ is a valid character&nbsp;JavaScript. It can be used as a variable name.</p>
<p>A function in JavaScript can be assigned to a variable name.&nbsp;</p>
<p>JavaScript is a case-sensitive language. All lines in JavaScript end with ;'s just like Java.</p>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>What does the function below do? Answer in a comment in your JavaScript file.</p>
<pre>var $ = function (id) {<br />&nbsp; &nbsp;return document.getElementById(id); <br />}</pre>
<p>&nbsp;</p>
<p>For this assignment you will create a sales tax application that uses JavaScript. There is also a css file which controls the display of the textboxes, etc.</p>
<p>Create a new Dynamic Web Application in Eclipse and import the code from</p>
<p><a href="https://github.com/dave45678/SalesTaxCalculator">https://github.com/dave45678/SalesTaxCalculator</a></p>
<p>&nbsp;</p>
<p>You need to only modify the .js file. You need to create a function called&nbsp;<strong>calculate_click</strong> which will retrieve the subtotal value and retrieve the tax rate value. Both these values will be entered in text boxes by the user.&nbsp;</p>
<p>Next, clear the salesTax textbox value and clear the total textbox value.</p>
<p>Then, check if the subtotal is numeric (use the JavaScript function called isNaN(subtotal). Also check if the subtotal is &gt;0. Alert the user if this isn't the case.</p>
<p>Do the same thing fro the taxRate.</p>
<p>If the user entered values are good then:</p>
<p>Calculate the salesTax as the subtotal times the taxRate divided by 100 and&nbsp;calculate the total as the sum of the subtotal and the salesTax.</p>
<p>Finally set the value of the salesTax and total text boxes to their respective values.</p>
<p>For the total, you can set the number of decimal places to 2 by calling total.toFixed(2).</p>
<p>&nbsp;</p>
<p>One last thing....</p>
<p>add the folllowing function to the end of your JavaScript file. In the function put a comment describing what does.</p>
<pre>window.onload = function () {<br /> $("calculate").onclick = calculate_click;<br /> $("subtotal").focus;<br />}</pre>
<p>&nbsp;</p>
<p>&nbsp;</p>
<p>&nbsp;</p>