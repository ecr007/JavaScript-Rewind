# Events

Event Handling is key for JavaScript interactivity.

## Typical DOM Events

- eventTarget.addEventListener(eventType, callbackFn) : Registers an event handler of a specifict event type on the event target. 

Source: https://developer.mozilla.org/en-US/docs/Web/Events

**How to get the element of target after event**

```js
e.currentTarget
this
```

**List of Events**

- click: Occurs when an element is clicked.

- change: Occurs when a value of an input element change.

- input: Occurs when the value of an input of textarea element changes. (Good to detect the change)

- select: Occurs when text within a text input o textarea is selected.

```js

const element = document.querySelector('#city');

const action = () => {
    console.log("New Value", this.value);
}

element.addEventListener("change", action);
```

- keydown: occurs when a key on the keyboard is pressed down. (Use form elements)

```js
element.addEventListener("keydown", (e) => {console.log("Key =>", e.key)})
```

- mouseeneter and mouseleave: Occurs when mouse pointer enters or leaves an elements.

- submit: Occurs when a form is submitted. 

```js
formElement.addEventListener("submit", (e) => {
    e.preventDefault();
    console.log("Form was submitted");
})
```

- load: Occurs when the entire page is loading. Include all image and others resources.

```js
windows.addEventListener("load", function(){
    // Run anything...
});
```

- focus and blur: Occurs when a element gains or loses focus. 

- mousemove: Occurs when the mouse pointer moves over an element. (Check the event parameters ```e.clientX``` and ```e.clientY```)

- resize: Occurs when the browser windows is resized.

```js
windows.addEventListener("resize", function(){...});
```

- window.scroll: Occurs when the user scroll the page.

- contextmenu: Occurs when the right mouse button is clicked. Typically to show a custom context menu.

```html
<div id="myDiv" oncontextmenu="return false;" style="width: 200px; height: 200px; background-color: lightblue;"></div>

<script>
    var myDiv = document.getElementById('myDiv');

    myDiv.addEventListener('contextmenu', function(event) {
        alert('Context menu triggered!');
        event.preventDefault(); // Prevent the default context menu
    });
</script>
```
- doubleclick: Occurs when an element is double-clicked.

- touchstart, touchmove, touchend, and touchcancel: These events are triggered by touch interactions on touch-enabled devices. ```touchstart``` occurs when a touch begins, ```touchmove``` occurs when the touch position changes, ```touchend``` occurs when the touch ends, and touchcancel occurs if the touch is canceled.

```html
<div id="touchDiv" style="width: 100px; height: 100px; background-color: lightblue;"></div>

<script>
    var touchDiv = document.getElementById('touchDiv');

    touchDiv.addEventListener('touchstart', function(event) {
        console.log('Touch started!');
    });

    touchDiv.addEventListener('touchmove', function(event) {
        console.log('Touch moved!');
    });

    touchDiv.addEventListener('touchend', function(event) {
        console.log('Touch ended!');
    });

    touchDiv.addEventListener('touchcancel', function(event) {
        console.log('Touch canceled!');
    });
</script>

```
