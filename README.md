# JavaScript Rewind

## NPM, WebPack And Gulp
Packages Manages.

## Node JS
Server runtime used to run JavaScript everywhere; used to run npm, webpack, babel and more on your computer. 

## Tools

- Live Server: for Visual Studio Code
- ESLint: Helps automatically detect coding errors and can do basic clean up automatically.
- Prettier: Helps automatically clean up your formatting. 

## Modern JavaScript Loading

```html
<!-- Browser downloads JavaScript in parallel while HTML renders. When JavaScript is fully loaded, rendering stops while JavaScript is executed.   -->
<script src="anyscript.js" async></script>

<!-- Browser downloads JavaScript in parallel while HTML renders. Then defers execution of JavaScript until HTML rendering is completed. -->
<script src="anyscript.js" defer></script>
```
**Async**
<img src="img/async-loading.png" />

**Defer**
<img src="img/defer-loading.png" />

**Important**
Loading JS file in footer is now anti-pattern, the best form is inside the head tag with [async|defer] parameters.

## JavaScript Modules

**Steps to use import**

Modules enables modularitation of code where individual function, components, data object, and other parts can be separated into individual files.

Use type=module instead defer

```html
<script src="main.js" type="module"> 
```

```javascript
// sum.js

// one export | default
function sum(){}
export default sum;

// helpers.js
// many export
export {one, two, three};

// main.js
import sum from "./sum.js";

import * as helpers from "./helpers.js";
// or
import {one, three} from "./helpers.js";
```
