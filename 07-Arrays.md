# Arrays

Is a collection creates with different kind of data or the same.

## Important methods to work with them.

- .push(...): Add one or more elements to the end of an array.

```javascript
let cars = ["Honda","Toyota"];
cars.push("Hyundai");
```

- .pop(): Remove the last element from an array.

- .shift(): Remove the first element from an array.

- .unshift(...): Add one or more element to the biginning of an array.

```javascript
cars.unshift("Ford","GMC");
```

- .splice(indexToStart, countToDelete, item1, ... , itemN): Changes the content of an array by removing or replacing existing elements or adding new elements.

```javascript
cars.splice(2,1,"Mazda","Nissan");

// To remove an element from an array
cars.splice(index, 1);
```

- .slice(intStart, intEnd) : returns a shallow copy of a **portion** of an array into a new array object selected from start to end. 

- .concat(array1, array2, ... , arrayN): combines two or more arrays and return a new array.

```js
let chineseCars = ["Changan","BYD","NIO"];
let allCars = cars.combine(chineseCars);
```

- .indexOf("Value to find") : returns the **first** index at whitch a given element can be found in the array, or -1 it it is not present.
- .lastIndexOf("Value to find") : returns the **last** index at whitch a given element can be found in the array.

```js
let index = cars.indexOf("Honda"); // 0
let anotherIndex = cars.indexOf("Kia"); // -1
```

- .includes("Value to find") : Checks if an array includes a certain element and return true or false.

- .forEach(item => {} or callbackFn) : Executes a provided function onece for each array element.

- .map(callbackFn) : creates a new array by applying a provided function to every element in the array. Return a new array. 

- .filter(callbackFn) : creates a new array with all elements that pass a test implemented by the provided function. 

```js
let onlyChinese = allCars.filter(car => {
    return chineseCars.includes(car);
});
```

- .reduce(callbackFn, initialValue = 0): Applies a function against an accumalator and each element in the array (from left to right) to reduce it to a single value.

```js
let numbers = [1,2,3,4];
let initialValue = 0;

let total = numbers.reduce((num_1, num_2) => {
    return num_1 + num_2
}, initialValue); // 10

// if the initial value is 5, the last result for total is 15
```

- .every(callbackFn) : Tests whether **all** elements in the array pass the provided function's test. It returns a boolean value.

```js
[1,2,3].every(function(item){
    return item > 5;
}); // false.
```

- .some(callbackFn) : Test whether at least one element in the array passed the provided function's test. 

```js
cars.some(car => car == "Honda"); // True, because honda is presents. 
```

- .find(callbackFn) : returns the first elements in the array that satisfies the provided testing function. 

- .reverse() : Reverses the elements of an array in place.

- .sort() : Sorts the elements of an array in place. 

- .join("separator") : Returns all elements of an array into a string. It returns empty string if array is empty.

