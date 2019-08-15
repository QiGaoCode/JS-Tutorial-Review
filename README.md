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

**JS Reference HTML DOM Events for more details**

Event | Description
--- | ---
onchange	 | An HTML element has been changed
onclick |	The user clicks an HTML element
onmouseover |	The user moves the mouse over an HTML element
onmouseout |	The user moves the mouse away from an HTML element
onkeydown	| The user pushes a keyboard key
onload	| The browser has finished loading the page

## JS String Method

String methods help to work with strings,

Note, in JS, methods and properties are available to primitive values, because JS treats primitive values as objects when executing methods and properties.

```javascript
var txt = "GQ is good at study, GQ";
// the length property returns the length of a string
var len = txt.length;

// the indexOf() method returns the index of ( position of ) the first occurrence of a text
var pos = txt.indexOf("is"); // output 3, space also account, position start from 0.


// the lastIndexOf() returns the index of last occurence

var pos1 = txt.lastIndexOf("is"); // output 22
// note both indexOf(),lastIndexOf() return -1 if the text is not found.
// both method accepts a second parameter as the starting position. ex . lastIndexOf("is", 15); 15 is the start postion.

// search() method search a string for a specified value and returns the position of match.
var pos3 = txt.search("is");

// slice(start,end)
var res = txt.slice(0,2) // output GQ 
// if the parameter is negative, the position is counted from the end of the string.

// substring(start,end)
var res1 = txt.substring(0,2) // output GQ , the difference is that substring do not accept negative value.

// substr(start, end)
// similar to slice(), but the second parameter specifies the length of the extracted part.
var res2 = txt.substr(0,1) // output "G"
// if first parameter is negative, position counts from the end of the string

// replace() methods replace the value with another value
var txt1 = txt.replace("GQ","Helen"); 
// by default, replace() is case sensitive.
// to replace case insensetive, use regular expression with an /i flag(insensitive):
var txt1 = txt.replace(/GQ/i, "Helen);
// to replace all matches, use a regular expression with a /g flag(global match)
var str = "GQ GQ is good";
var n  = str.replace(/GQ/g, "Helen");

// toUpperCase()
// toLowerCase()

// concat() joints two or more strings:
var txt5 = "Hello";
var txt6 = "World";
var txt7 = txt5.concat("",txt6);

// trim() remove whitespaces from both sides of a string
var ex = "         Hello World              ";
ex.trim();

// Extarcting String Character
// charAt(position) RETURN TEH character at index
// charCodeAt(position) return the unicode of the character 
// property Access []

txt.charAt(0); // return "G"
txt[0]; // return "G"
```

**Converting A String to an Array

use split() method

```javascript
var ex1 = "a,b,c,d"; // string
ex1.split(","); //split on commas
ex1.split(" "); //split on space
ex1.split("|"); //split on pipe

var ex2 = "hello" 
ex2.split("") // split in character

```

## JS numbers

NaN - not a number

**NaN** is a JavaScript reserved word indicating that a number is not a legal number.

typeof NaN returns number

**Infinity** is the value JavaScript will return if you calculate a number outside the largest possible number

typeof Infinity return number

Number can be objects

var x = 123;

var y = new Number(123);

## JS number methods

The toString() method returns a number as string

The toExponential() method

```javascript

var x = 9.656
x.toExponential(2); // return 9.66e+0
x.toExponential(4); // return 9.6560e+0

// the toFixed() method
// toFixed() return a string, with the number written with a specified number of decimals:
var x = 9.656;
x.toFixed(0); // return 10
x.toFixed(2); // return 9.66
x.toFixed(4); // return 9.6560

// toPrecision() method
// toPrecision() returns a string, with a number written with a specified length
x.toPrecision(); // return 9.656
x.toPrecision(2);// return 9.7

// valueOf() Method
// valueOf() return a number as a number
x.valueOf(); // return 123 from x

```

**Converting Variable to Numbers**
- the Number() method
- the parseInt() method
- the parseFloat() method


```javascript
Number(true); // return 1
Number(false); // return 0
Number("10"); // return 10
Number("19,33") // return NaN


// parseInt() parses a string and returns a whole number. spaces are allowed. only the first number is returned
parseInt("10"); // output 10
parseInt("10.33") // output 10
parseInt("10 29 30") // output 10
parseInt("year 10") // output NaN
```

## Arrays

var array_name = [item1, item2, item3, ....];

var array_name = new Array(item1, item2, item3, ...);

Note Arrays are a special type of object.

Arrays use numbers to access its element, ex, person[0] return John

var person = ["John","Doe",43];

Array use names to access its element. person.firstName returns John

var person = {firstName: "John", lastName: "Doe", age: 43};

**Looping Array Elements**

- for loop

- Array.forEach()
 ```javascript
 var fruits, text;
 fruits = ["Banada", "Orange","Apple"];
 
 fruits.forEach(myFunction);
 
 function myFunction(value){
   text += value;
 }
 ```
push() method to add array element

In JS, arrays use numbered indexes. should use arrays when you want element names to be numbers.

In JS, objects use named indexes. should use objects when you want the element names to the strings(text).

## Array Method

toString() converts an array to a string of array values,

pop() remove the last element, return the value that was popped out

push() add element to array, return the new array length

shift() remove the first element, return the string that was shiffed out.

unshift(item) add new element to array at first, and return the new length

splice() add new items to an array.

var fruits = ["Banana","Orange","Apple","Mango"];
fruits.splice(2,0,"Lemon","kiwi");

first parameter define position where new element add,

second parameter define how many elements should be removed.

use splice() to remove elements without leaving holes in array,

concat() creates a new array by merging existing arrays.

var A = ["1"];
var B = ["2"];
var c = A.concat(B);

slice() slices out a piece of an array into a new array.

slice (number)  or slice(number, number) 

sort()

reverse()

sort ascending

var points = [1,2,3,4,5,6,7,8]
points.sort(function(a,b){return a - b});

points.sort(function(a,b){return b - a});

Math.max.apply(null, arr) to find the highest number

Math.min.apply(null, arr) to find the lowest number.




## Array Iteration

## JavaScript Type Conversion


5 different data types that can contain values:

-string
-number
-boolean
-object
-function

6 types of object

-object
-Date
-Array
-String
-Number
-Boolean

2 data type cannot contain values:

-null
-undefined



