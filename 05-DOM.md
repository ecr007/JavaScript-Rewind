# DOM

- document.querySelector("CSS Selector"): returns the first elements within the document that matches the specified selector, or group of selector, if not matches are found, ```null``` is returned. 

- document.querySelectorAll(): returns a static not live, NodeList representing a list of document's elements that match the specified group of selectors.

- document.getElementsByClass("class_name") : Returns a list of element in HTMLCollection (CSS selectors are not support) (A little deprecated)

- document.getElementById("id_name"): gets a element by an ID (CSS selectors are not support) (A little deprecated)

```javascript
// Arrow function example
const list = document.querySelectorAll("Any Selector");

list.forEach( item => {
    item.style.background = "red";
    item.style.cssText = "Custom CSS";
});

//  Or

list.forEach(item => item.style.background = "red");

//  Documentation
// https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions
```

- Element.style.background = "red": Set background color to element.

## Modifying Element Clasess With classList

- Element.classList: is a Read-Only property that returns a live ```DOMTokenList``` collection of the ```class``` attributes of the element. this can then be used to manipulate the class list. 

**Available Methods**

```javascript

const content = document.querySelector(".content");

// Add
content.classList.add("col-xs-12");

// Remove
content.classList.remove("col-sm-12");

// Replace
content.classList.replace("col-xs-12","col-md-6");

// Toggle: Add and Remove
content.classList.toggle("col-sm-12");

```

source: https://developer.mozilla.org/en-US/docs/Web/API/Element/classList

**Alternative to classList**
- Element.className: Is an alternative but classList is the best.

## Attributes Collection

- Element.attributes: Property returns a live collection of all attribute nodes registered to specific node. 

**Related Methods**

- Element.hasAttribute()
- Element.setAttribute(name, value)
- Element.removeAttribute()

## Add DOM Elements

- document.createElement(name, option): Method creates the HTML element specified by tag name, or an HTMLUnknownElement if tagName isn't recognized. 

```javascript

const list = document.createElement("ul");
list.classList.add("ecr-dotted");
list.setAttrinute("id", "ecr-main-list");

// Set Items

const main = document.querySelector("#main");

// Append
main.append(list)
```
**Inserts**

- Element.append(p1,p2, /* ..., */ pN): Method inserts a set of Node objects or string objects after the last child of the elements. 

- Element.prepend(p1,p2, /* ..., */ pN) Method inserts a set of Node objects or string objects before the first child of the elements.

- Element.insertAdjacentElement(position, element): Method of the element interface inserts a given element Node at a given position relative to the elements it is invoked upon. 

**Positions**

```html
<!-- beforebegin -->
<p>
  <!-- afterbegin -->
  foo
  <!-- beforeend -->
</p>
<!-- afterend -->
```