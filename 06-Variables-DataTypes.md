# Variables and Data Types

var: Declares function-scope or globally-scope 

let: Declares re-assignable, block-scoped local variable, cannot be redeclarate. 

const: Declares block-scoped local variable. The value of a constant can't be changed through reassignment using the assignment operation. But if a constant is an object, its properties can be added, updated or removed.

## Data type
Use ```typeof``` to get the type of an object.

```
const Car{
    branch: "Honda",
    model: "Civic",
    year: 2018,
    price: 14480,
}

console.log("Type of Car is", typeof Car);
```

## Math Operations

```javascript

// Exponentiation
var results = 3 ** 2;
// Also its possible use Math class
var results = Math.pow(3,2);

// Percentage Symbol or Modulo named
// It gives us the remainder left over when we divide the first number by the second number.
var results = 10 % 2; // 0
var results = 9 % 2; // 1 (8 / 2)
var results = 15 % 10 // 5 

// Error when we add number to string  or in other way, to prevent it use Number cast.
var a = "50";
var b = 50;
console.log(a+b); // '5050'

// Convert value to number
var fix = Number(result);

// Check if it a number
if (!isNaN(fix)) // ... True is a number, or false isn't a number

// Incremented or Decremented by one
var i = 15;

// Sum one
console.log(++i); // 16

// Otherwise
console.log(i++); // 15
console.log(i); // 16

// Take one away from that number
console.log(--i); // 14

// toFixed(number)
// This method remove number after point for decimal or float datatype
var isNumber = 50.3054;
console.log(isNumber.toFixed(1)); // 50.3

// Remeber
parseInt()
parseFloat()
```

Note: String Combiner is when you concatate two or more string with plus (+)

**Snippets**
```javascript
// How to Get Randmon element of an array 
const ary = [1,2,3,4,5,6];

var key = Math.floor(Math.random() * ary.length)
console.log(ary[key]);

// 
```

Source: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math