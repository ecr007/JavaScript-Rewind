# Functions and Methods

There are couple form to creare a function.

**Function Declaration**
```js
function anyFunctionality(){}
```


**Function Expression**
```js
const anyFunctionality = function(){};
const anySecFunctionality = (param) => {};
```

Function expression is the best option because is inside a const, and it is locally scoped or block scoped. It also cannot be re-declared. So you're never in danger accidentally overwriting or destroying your function. 

**Immediately Invoked Function Expression (IIFE)**
(Anti-pattern)
(Also named Anonymous function)
(Arrow function is also named anonymous function)

```js
// This function is hoisted out of the object and up the global scope.
(function(){
    // Run any functionality, it does not need callback.
})();
```

## Important to see

<img src="img/functions.png" alt="Arrow-vs-Functions"/>

## Internation Number Format With (Intl class)

The ```Intl.NumberFormat``` object enables leanguage-sensitive number formatting.

Source: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Intl/NumberFormat

```js

const formatter = (value, lang, currency) => {
    return (
        new Intl.NumberFormat(lang, {
            style: "currency",
            currency: currency
        }).format(value)
    );
}

let num = 896523.584;

console.log(`
    Your anually salary is: ${formatter(num, "en-US", "USD")}
`);

// Response: $896,523.58

```