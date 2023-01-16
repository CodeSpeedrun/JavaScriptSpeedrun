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

```

##JavaScript Events

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
