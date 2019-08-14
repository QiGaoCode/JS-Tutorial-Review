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

numbers are written with or without decimals. EX: 10.50  1001

Strings are text, written within double or single quotes. EX: "Eric", 'Eric'.


**JavaScript and Camel Case**

Hyphens: (连字符） are not allowed in JavaScript, they are reserved for subtractions. ex: first-name

undersocre: _  

Upper Camel Case ( pascal case) 

Lower Camel Case:

Javascript tend to use camel case that start with a lowercase letter: EX: firstName.

## JS comments

//

/*

asdnalsjdlkasjdasdnaskdhlasjdklas

sdasdadasdasd

*/


## JS Variables

JS have many data types: numbers, strings, objects, boolean

a variable declared without a value will have the value undefined.

```javascript
var carName; // carName undefined
var x = "5" + 2 + 3 ;
// output 523, if put a number in quotes, the rest of numbers will be treated as strings, and concatednated.
var x = 2 + 3 + "5";
// output "55"
```

## JS Data Types

```javascript
var length = 16;      // Number
var lastName = "Gao"; // String
var x = {firstName: "Qi", lastName: "Gao"}; // Object
```

Note JavaScript has dynamic types. which means same variable can be used to hold different data types.

**JS Arrays**

arrays are written with square brackets. []

array items are separated by commas.

```javascript
var cars = ['bmw','volvo','audi'];
```

**JS Objects**

objects are written with curly braces {}.

object properties are written as name: value pairs, separated by commas.

```javascript
var person = {firstName: "Qi", lastName: "Gao", age:50, eyeColor: "black"};
```

**typeof Operator**
```javascript
typeof "" // output "string"
typeof 3.14 // output "number"
car = undefined; // value is undefined, type is undefined.
var car = ""; // the value is "", but the type is "string".
```
**Null**

In JS, null is nothing. the data type of null is an object

```javascript
var person = {firstname: "QI", lastName: "Gao"};
person = null; // now value is null, but type is still an object

var person = {firstname: "QI", lastName: "Gao"};
person = undefined; // now both value and type is undefined
```

**Difference Betweeen undefined and null

```javascript
typeof undefined    //undefined
typeof null     //object

null === undefined  // false
null == undefined // true
```

**Primitive Data**
 
The typeof return one of : string, number, boolean, undefined

**Complex Data**

the typeof return one of : function , object

```javascript
typeof {name:"Qi", age: 34} // return object
typeof [1,2,3,4]            // return object (not "array"), note in js, array is object
typeof null                 // return object
typeof function myFunc(){}  // return function
```

## JS Functions

**JS function Syntax**

A JS function is defined with **function** keyword, followed by a name, followed by parenthese().

function name can contain letters, digits, underscores, and dollar signs, the parantheses may include parameter names separated by commas: (parameter1, parameter2, ...)

```javascript
function name (parameter1, parameter2, parameter3){
  // code to be executed
}
```

when js function reaches a **return** statement, the function will stop executing.

**Why use Functions**

- can reuse the code
- can use the same code many times with different arguments, to produce different results.

**() operator invokes the function

```javascript
function add(resuilt){
 return (5/9)*(result - 32);
}
document.getElementById("demo").innerHTML = add;
```

Note access a function without () will only return the function definition instead of function result.

**Local Variable**
```javascript
// cannot use carName

function myFunction(){
  var carName = "Volvo";
  // code here can use carName
}

// cannot use carName
```

## JavaScript Objects

**Object Definition**

define a JavaScript object with an object literal

```javascript
var person = {
 firstName : "Qi",
 lastName: "Gao",
 age: 40,
 eyecolor: "Black"
};
```

**Access Object Properties**

objectName.propertyName

or

objectName["peopertyName"]


**The this keyword**

in a function definition, this refer to the owner of the function,

- in a method, this refer to the owner object
- alone, this refer to the global object.
- in a function, this refer to the global object.
- in a function, in strict mode, this is undefined.
- in an event, this refer to the element that received the event
- methods like call(), apply(), can refer this to any object.


**Do not declare strings, numbers, booleans, as objects**

when a js variable is declared with keyword **new**, the variable is created as an object.

## JS events.

Event | Description
--- | ---
onchange	 | An HTML element has been changed
onclick |	The user clicks an HTML element
onmouseover |	The user moves the mouse over an HTML element
onmouseout |	The user moves the mouse away from an HTML element
onkeydown	| The user pushes a keyboard key
onload	| The browser has finished loading the page
