###JavaScript is a real language

JavaScript ("JS" for short) is a full-fledged dynamic programming language. JavaScript provides dynamic interactivity on websites. JavaScript is compact but flexible. Many tools have been written on top of the JavaScript language allowing one to add functionality with minimal effort. 

JavaScript may be the most misunderstood programming language in the world. It combines simplicity with power. It is often misused. JavaScript is finding its way into more and more high-profile applications and gaining acceptance.

####Developer Tools
Let's try some JavaScript examples in the browser. You can save these examples to a web page in the body section. Refresh the page after each edit to see your changes. 

If you are using Chrome or Firefox  you can open the developer tools. From there you can view the console. You may wish to browse to a blank page so type "about:blank" in the address bar. 

Do you need information about using the developer tools?
* Chrome: ```https://developer.chrome.com/devtools``` 
* Firefox: ```https://developer.mozilla.org/en-US/docs/Tools```

Type the following in the developer tools console. If you are working from a web page then the JavaScript code needs to be between ```<script> ... </script>``` tags. The script tags can go inside the body. You'll have to save and refresh the page with every change. 
```html
document.write('hello, world!');
```

Let's start with variables. A variable has a name and contains a value. Use the ```var``` keyword followed by the name. Do not define a type. JavaScript will determine the type once you give it data. Until then it will be undefined. 
```html
//this is a comment. It will not be executed
var myVar = 5;
document.write(myVar);
document.write("<br/>")
```

JavaScript uses the ```+``` to concatenate strings. 

```html
var words = "This sentence ends in a";
var moreWords = " preposition.";
var sentence = words + moreWords;
//go to the next line
document.write(sentence + '<br/>');
```
JavaScript needs you to escape quotes inside strings. Use the ```\``` to escape the single quote. If your string has double-quotes then you don't have to escape a single quote inside of it.

```html
//using double or single quotes
var s = 'A string that\'s single quoted'
document.write(s);
document.write("<br/>")

s = "A string that's double quoted"
document.write(s);
document.write("<br/>")
```
Since JavaScript strings are objects they have properties and methods you can access. Here is an example of returning the length property or executing the substring method. For documentation about these and other string properties and methods refer to any of the various online sources. I recommend ```https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/About```.

```html
document.write(sentence.length);
document.write("<br/>")
```
Strings also have methods
```html
document.write(sentence.substring(2,5);
```

####JavaScript Arrays

The JavaScript Array object is a global object that is used in the construction of arrays; which are high-level, list-like objects.

Here's how you declare an array and print the first item:

```html
var simpsons = ['homer','marge','lisa','bart'];
document.write("<br/>")
document.write(simpsons[0]);
document.write("<br/>")
```

Now sort the array and display it:
```html
simpsons.sort();
//display the array
for (var i = 0; i < simpsons.length; i++){
	document.write(simpsons[i]);
}
```
The length property of the array returns a count of the number of items it contains. Since arrays are zero-based the last item will have an index value of one less than the length. Access the last item as shown below:

```html
var last = simpsons[simpsons.length - 1];
document.write(last);//bart
```

In the next example I show you how to use push to add a new item. The opposite of push is pop which will remove it.

```html
var donnie = simpsons.push('Donnie');
document.write(simpsons);
simpsons.pop();
```

Remove element at a specific index 
```html
delete a[4];
//display the array
for (var i = 0; i < a.length; i++){
	document.write(a[i])
}
```
Just like in many other programming languages, you can populate an array from a for loop.

```html
var numbers = [];
for (var i = 0; i < 10; i++){
	numbers[i] = i + 1;
}
//display the array
for (var i = 0; i < 10; i++){
	document.write(numbers[i]+"<br/>");
}
```

####JavaScript Functions

JavaScript lets you define your own functions with the keyword, function. 
It's a good idea to put the function in the head tags to keep things organized.

```html
function sayAnything(what){
	document.write(what);
}
//call the function
sayAnything("anything");
```

JavaScript allows you to assign a function to a variable so calling the variable is like calling the function.
```html
var say = saySomething();
```

Sometimes functions are assigned to a the '$' which is a valid character for variable names. JQuery does this as you'll see.

```html
<input type="text" id="element"></input>
var $ = function (id){
    return document.getElementById(id);
}
```
You can set the value of the element by the function. If the element was a paragraph this function would return a reference to it.
```html
$("element")
//return an element by id
document.write($("element"));
```

####Decision making in JavaScript
```html
var a = 7
if (a > 10){
// do something
}else{
// do something else
}
```

###repetition/looping
```html
for(i=0;i<5;i++){
document.write("this is iteration number " + i + "<br/>");
}
```
```html
while (c < 10) {
  c += 1;
  // …
}
```
```html
while (c < 10) {
  c += 1;
  // …
}
```

####Getting input from user
You can read an element with that contains user-entered text as follows:
```var text=document.getElementById('input1').value;```

You can display a message or set the text of an element:
```document.getElementById("message").innerHTML = "some text";```


//date

//modifying the DOM

//getting input by prompting the user
//determining if the user clicked cancel p. 225

//get the state of a radio button 229
//get the state of a checkbox 231
//reading user input from text areas 235

//focus and blur 235

//common control events 237

//how to display output 239

//display data in a text area 245

//working with numbers 251

//the conditional operator 255


//working with Strings 261

//comparing two strings 265

//dates and times 267
//create a date object 267
//methods of a date object 269
//how to calculate a due date 271
//how to find the end of the month 271



</script>

<hr/>
<script>
var cody = new Object();
cody.living = true;
cody.age = 33;
cody.gender = 'male';
cody.getGender = function () { return cody.gender; };
console.log(cody.getGender()); // Logs 'male'.
</script>

<script>
document.write("Hello world!\n\n");
var output = '',
    i;
for (i = 2; i <= 8; i += 2) {
   output += i + ', ';
}
output += 'who do we appreciate?\n\n';
document.write(output);

function isPalindrome(str) {
  return str === str.split("").reverse().join("");
}
 
console.log(isPalindrome("ingirumimusnocteetconsumimurigni"));

</script>

JavaScript uses scope chains to establish the scope for a given function. There is typically one global scope, and each function defined has its own nested scope. Any function defined within another function has a local scope which is linked to the outer function. It's always the position in the source that defines the scope.

An element in the scope chain is basically a Map with a pointer to it's parent scope.

When resolving a variable, javascript starts at the innermost scope and searches outwards.
```html
<script>
// a globally-scoped variable
var a=1;
 
// global scope
function one(){
    document.write(a); 
}
 
// local scope
function two(a){
    document.write(a);
}
 
// local scope again
function three(){
  var a = 3;
  document.write(a);
}
 
// Intermediate: no such thing as block scope in javascript
function four(){
    if(true){
        var a=4;
    }
 
    document.write(a); // alerts '4', not the global value of '1'
}
 
 
// Intermediate: object properties
function Five(){
    this.a = 5;
}
 
 
// Advanced: closure
var six = function(){
    var foo = 6;
 
    return function(){
        // javascript "closure" means I have access to foo in here, 
        // because it is defined in the function in which I was defined.
        document.write(foo);
    }
}()
 
 
// Advanced: prototype-based scope resolution
function Seven(){
  this.a = 7;
}
 
// [object].prototype.property loses to [object].property in the scope chain
Seven.prototype.a = -1; // won't get reached, because 'a' is set in the constructor above.
Seven.prototype.b = 8; // Will get reached, even though 'b' is NOT set in the constructor.
 
 
 
// These will print 1-8
one();
two(2);
three();
four();
document.write(new Five().a);
six();
document.write(new Seven().a);
document.write(new Seven().b);
</script>


<script>
function guessNumber() {
  // Get a random integer from 1 to 10 inclusive
  var num = Math.ceil(Math.random() * 10);
  var guess;
 
  while (guess != num) {
    guess = prompt('Guess the number between 1 and 10 inclusive');
  }
  alert('Congratulations!\nThe number was ' + num);
}
 
//guessNumber();


//dom scripting 425

</script>
```
