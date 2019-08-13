# JS-Tutorial-Review
The summary of the JavaScript 

# JS Tutorial

HTML: define the content of the web pages

CSS: Specify the layout of the web pages

JavaScript: program the behavior of the web pages.

## JS where to
External JavaScript Advantages
- separates HTML and code
- make HTML and JavaScript easier to read and maintain
- Cached JavaScript Files can speed up page loads.

Use
```javascript
<script src = "myScript1.js"> ... </script> 
// External Scripts can be referenced with a full URL or with a path relative to the current web page
```

## JS Output

- write into HTML element, using innerHTML.
- write into the HTML output, using document.write().
- write into an alert box, using window.alert().
- write into the browser console, using console.log().

Example:

```javascript
document.getElementById("demo").innerHTML = 5 + 6;
document.write(5+6);
//for testing purpose, Note, Using document.write() after an HTML document is loaded, will delete all existing HTML.
```

## JS Statement

A JavaScript program is a list of programming statements, and is executed by the web browser.

**Values, Operators, Expressions, Keyword, and Comments**


##### JS code Blocks

code blocks, inside curly brackets {...}

##### JS keywords.

Keyword | Description
--- | ---
break |	Terminates a switch or a loop
continue |	Jumps out of a loop and starts at the top
debugger | Stops the execution of JavaScript, and calls (if available) the debugging function
do ... while |	Executes a block of statements, and repeats the block, while a condition is true
for |	Marks a block of statements to be executed, as long as a condition is true
function |	Declares a function
if ... else |	Marks a block of statements to be executed, depending on a condition
return |	Exits a function
switch |	Marks a block of statements to be executed, depending on different cases
try ... catch |	Implements error handling to a block of statements
var |	Declares a variable

## JS Syntax

JavaScript Syntax defines two type of values : Fixed values and variable values.

Fixed values are called literals, variable values are valled variables.

**JS Literals**
numbers are written with or without decimals.

