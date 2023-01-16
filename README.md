## Variables
If you want a general rule: always declare variables with const.
If you think the value of the variable can change, use let.
A variable without a value has the value of: undefined
```xxx 
const pi = 3.14;
let person = "John Doe";
```

## JavaScript Const
Use const when you declare:
A new Array
A new Object
A new Function
A new RegExp
```xxx
const cars = ["Saab", "Volvo", "BMW"];
// You can change an element:
cars[0] = "Toyota";
// You can add an element:
cars.push("Audi");

const car = {type:"Fiat", model:"500", color:"white"};
// You can change a property:
car.color = "red";
// You can add a property:
car.owner = "Johnson";
```

## JavaScript Type Operators
typeof	=> Returns the type of a variable
instanceof =>	Returns true if an object is an instance of an object type
```xxx
&&	logical and
||	logical or
!	logical not

==	equal to
===	equal value and equal type
!=	not equal
!==	not equal value or not equal type
>	greater than
<	less than
>=	greater than or equal to
<=	less than or equal to
?	ternary operator

+	Addition
-	Subtraction
*	Multiplication
**	Exponentiation (ES2016)
/	Division
%	Modulus (Division Remainder)
++	Increment
--	Decrement
 
The exponentiation operator (**) raises the first operand to the power of the second operand.
Example
let x = 5;
let z = x ** 2;

x ** y produces the same result as Math.pow(x,y):
Example
let x = 5;
let z = Math.pow(x,2);
```

## JavaScript Data Types
JavaScript has 8 Datatypes
1. String
2. Number
3. Bigint
4. Boolean
5. Undefined
6. Null
7. Symbol
8. Object

The Object Datatype
The object data type can contain:

1. An object
2. An array
3. A date


```xxx
let length = 16;
let weight = 7.5;

// Strings:
let color = "Yellow";
let lastName = "Johnson";

// Booleans
let x = true;
let y = false;

// Object:
const person = {firstName:"John", lastName:"Doe"};

// Array object:
const cars = ["Saab", "Volvo", "BMW"];

// Date object:
const date = new Date("2022-03-25");

let car = "";    // The value is "", the typeof is "string"

```

##JavaScript Functions
When an event occurs (when a user clicks a button)
When it is invoked (called) from JavaScript code
Automatically (self invoked)

Accessing a function without () will return the function object instead of the function result.
```xxx
function toCelsius(fahrenheit) {
  return (5/9) * (fahrenheit-32);
}
document.getElementById("demo").innerHTML = toCelsius(77);

function toCelsius(fahrenheit) {
  return (5/9) * (fahrenheit-32);
}
document.getElementById("demo").innerHTML = toCelsius;
```

## JavaScript Objects
```xxx
<script>
// Create an object:
const person = {
  firstName: "John",
  lastName : "Doe",
  id     : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};

// Display data from the object:
document.getElementById("demo").innerHTML = person.fullName;
</script>
```

## What is this?
In JavaScript, the this keyword refers to an object.

Which object depends on how this is being invoked (used or called).

The this keyword refers to different objects depending on how it is used:

In an object method, this refers to the object.
Alone, this refers to the global object.
In a function, this refers to the global object.
In a function, in strict mode, this is undefined.
In an event, this refers to the element that received the event.
Methods like call(), apply(), and bind() can refer this to any object.

The this Keyword
In a function definition, this refers to the "owner" of the function.

In the example above, this is the person object that "owns" the fullName function.

In other words, this.firstName means the firstName property of this object.
```xxx
When using the === operator, x and y are not equal:
Comparing two JavaScript objects always returns false.
```

##JavaScript Events
onchange	An HTML element has been changed
onclick	The user clicks an HTML element
onmouseover	The user moves the mouse over an HTML element
onmouseout	The user moves the mouse away from an HTML element
onkeydown	The user pushes a keyboard key
onload	The browser has finished loading the page
```xxx
String length
String slice()
String substring()
String substr()
String replace()
String replaceAll()
String toUpperCase()
String toLowerCase()
String concat()
String trim()
String trimStart()
String trimEnd()
String padStart()
String padEnd()
String charAt()
String charCodeAt()
String split()

let text = "Apple, Banana, Kiwi";
let part = text.slice(-12);

let text = "Please visit Microsoft!";
let newText = text.replace("Microsoft", "W3Schools");

let text = "HELLO WORLD";
text[0] = "A";    // Gives no error, but does not work
```

## JavaScript Arrays
Arrays are a special type of objects. The typeof operator in JavaScript returns "object" for arrays.
You can also use the Array.forEach() function:

fruits.push("Lemon");  // Adds a new element (Lemon) to fruits
fruits[fruits.length] = "Lemon";  // Adds "Lemon" to fruits

In JavaScript, arrays use numbered indexes.  
In JavaScript, objects use named indexes.
```xxx
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript Arrays</h2>

<p>The best way to loop through an array is using a standard for loop:</p>

<p id="demo"></p>

<script>
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fLen = fruits.length;

let text = "<ul>";
for (let i = 0; i < fLen; i++) {
  text += "<li>" + fruits[i] + "</li>";
}
text += "</ul>";

document.getElementById("demo").innerHTML = text;
</script>

</body>
</html>

```

## JavaScript if .. else
```xxx
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript if .. else</h2>

<p>A time-based greeting:</p>

<p id="demo"></p>

<script>
const time = new Date().getHours();
let greeting;
if (time < 10) {
  greeting = "Good morning";
} else if (time < 20) {
  greeting = "Good day";
} else {
  greeting = "Good evening";
}
document.getElementById("demo").innerHTML = greeting;
</script>

</body>
</html>
```

## JavaScript switch

```xxx
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript switch</h2>

<p id="demo"></p>

<script>
let x = "0";

switch (x) {
  case 0:
    text = "Off";
    break;
  case 1:
    text = "On";
    break;
  default:
    text = "No value found";
}
document.getElementById("demo").innerHTML = text;
</script>

</body>
</html>
```

## JavaScript Errors
The try statement defines a code block to run (to try).

The catch statement defines a code block to handle any error.

The finally statement defines a code block to run regardless of the result.

The throw statement defines a custom error.
```xxx
hello = function() {
  return "Hello World!";
}

hello = () => {
  return "Hello World!";
}

hello = () => "Hello World!";
hello = (val) => "Hello " + val;

With a regular function this represents the object that calls the function:
// Regular Function:
hello = function() {
  document.getElementById("demo").innerHTML += this;
}
// The window object calls the function:
window.addEventListener("load", hello);
// A button object calls the function:
document.getElementById("btn").addEventListener("click", hello);

With an arrow function this represents the owner of the function:
// Arrow Function:
hello = () => {
  document.getElementById("demo").innerHTML += this;
}
// The window object calls the function:
window.addEventListener("load", hello);
// A button object calls the function:
document.getElementById("btn").addEventListener("click", hello);

```

## JavaScript Class Method


```xxx
<!DOCTYPE html>
<html>
<body>

<h2>JavaScript Class Method</h2>

<p>Pass a parameter into the "age()" method.</p>

<p id="demo"></p>

<script>
class Car {
  constructor(name, year) {
    this.name = name;
    this.year = year;
  }
  age(x) {
    return x - this.year;
  }
}

let date = new Date();
let year = date.getFullYear();

let myCar = new Car("Ford", 2014);
document.getElementById("demo").innerHTML=
"My car is " + myCar.age(year) + " years old.";
</script>

</body>
</html>

```

##
```xxx

```

##
```xxx

```

##
```xxx

```

##
```xxx

```

##
```xxx

```

##
```xxx

```

##
```xxx

```

<details id=1>
<summary><h2>Step 1</h2></summary>
 
</details>
