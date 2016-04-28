###JavaScript Examples
Let's try some JavaScript examples in the browser. You can save these examples to a web page in the body section. Refresh the page after each edit to see your changes. If you have Chrome or Firefox you can open the developer tools to view the console. You may wish to browse to a blank page so type "about:blank" in the address bar. If you need more information for using the developer tools in Chrome then visit ```https://developer.chrome.com/devtools``` or for Firefox visit ```https://developer.mozilla.org/en-US/docs/Tools```. 

Type the following in the console. If you want to type it in a web page then it needs to be between ```<script> ... </script``` tags.
```html
document.write('hello, world!');
```

A variable is has a name and contains a value. Use the var keyword followed by the name. Do not define a type. JavaScript will determine the type once you give it data. Until then it will be undefined.
```html
//this is a comment. It will not be executed
var myVar = 5;
document.write(myVar);
document.write("<br/>")
```

JavaScript uses the ```+``` to concatenate strings. 

```html
var words = "This sentence ends in a";
var moreWords = "proposition.";
var sentence = words + moreWords;
document.write(sentence + '<br/>');
```
You need to escape quotes inside strings ...
```html
//using double or single quotes
var s = 'A string that\'s single quoted'
document.write(s);
document.write("<br/>")

s = "A string that's double quoted"
document.write(s);
document.write("<br/>")
```

//strings have properties
document.write(sentence.length);
document.write("<br/>")
//strings have methods
document.write(sentence.substring(2,5);

//arrays  
var a = new Array[7];
a[0] = 'cat';
a[1] = 'dog';
a[2] = 95;
a[3] = true;

//or you can use a different notation
var simpsons = ['homer','marge','lisa','bart'];
document.write("There are " + simpsons.length + " Simpsons");
document.write("<br/>")
document.write(simpsons[0]);
document.write("<br/>")

//sort the array
simpsons.sort();
//display the array
for (var i = 0; i < simpsons.length; i++){
	document.write(simpsons[i]);
}

//add elements to an array 
a[4] = 'new value';

//display the array
for (var i = 0; i < a.length; i++){
	document.write(a[i])
}

//remove element at a specific index 
delete a[4];
//display the array
for (var i = 0; i < a.length; i++){
	document.write(a[i])
}

//populating an array from a for loop 
var numbers = [];
for (var i = 0; i < 10; i++){
	numbers[i] = i + 1;
}
//display the array
for (var i = 0; i < 10; i++){
	document.write(numbers[i]+"<br/>");
}


//define your own functions with the keyword, function
//good idea to put the function in the head tags to keep things organized
function sayAnything(what){
	document.write(what);
}

//call the function
sayAnything("anything");

//you can also assign a function to a variable
var say = saySomething();

//sometimes functions are assigned to a $
<input type="text" id="element"></input>
var $ = function (id){
    return document.getElementById(id);
}
//set the value of the element by the function
$("element")
//return an element by id
document.write($("element"));


//making decisions
var a = 7
if (a > 10){
//
}else{
//
}
//switch 287

//repetition/looping
//for loop 295
for(i=0;i<5;i++){
document.write("this is iteration " + i + "<br/>");
}

//while 291
//do while 293
//break statement 297

//getting input from user

//alert - prompting user

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

Javascript uses scope chains to establish the scope for a given function. There is typically one global scope, and each function defined has its own nested scope. Any function defined within another function has a local scope which is linked to the outer function. It's always the position in the source that defines the scope.

An element in the scope chain is basically a Map with a pointer to it's parent scope.

When resolving a variable, javascript starts at the innermost scope and searches outwards.
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
