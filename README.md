# Computer Apps II - Introduction to Javascript

- [Select Objects from HTML](#select-objects-from-html)
- [Events](#events)

## Select Objects From HTML

Use `document.querySelector()` to select elements from an HTML document using their ID

**HTML**
```html
<div id="button1">Apply</div>
<div id="button2">Reset</div>
```

**Javascript**
```javascript
let button1Elt = document.querySelector("#button1");
let button2Elt = document.querySelector("#button2");
```

### Pro-Tips:

- Don't forget the #
- Use `console.log` to test that you grabbed the element correctly

### Practice Repositories

[Lightbulb Selector](https://github.com/upperlinecode/lightbulb-selector-template)

## Events

Use `.addEventListener()` to an HTML element to make it _listen_ for an event. The syntax for an event looks like:
```javascript
____.addEventListener("____", (e) => {
  //Event code goes here
});
```
Some common events are:

- click
- mouseover
- movemove
- keypress
- change
- focus

The `e` variable holds event information. This is useful for detecting where a mouse click was or what key was pressed.

**Javascript**
```javascript
let divElt = document.querySelector("#divButton");
divElt.addEventListener("click", (e) => {
  console.log("Clicked on divButton");
});
```

### Pro-Tips

- Don't forget the closing `});` at the end
- Don't forget the `(e)`
