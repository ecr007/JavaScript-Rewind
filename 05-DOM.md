# DOM

- document.querySelector("CSS Selector"): returns the first elements within the document that matches the specified selector, or group of selector, if not matches are found, ```null``` is returned. 

- document.querySelectorAll(): returns a static not live, NodeList representing a list of document's elements that match the specified group of selectors.

```javascript
// Arrow function example
const list = document.querySelectorAll("Any Selector");

list.forEach( item => {
    item.style.background = "red";
});

//  Or

list.forEach(item => item.style.background = "red");

//  Documentation
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions
```

- domElement.style.background = "red": Set background color to element.