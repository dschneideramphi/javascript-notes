# Computer Apps II - Introduction to Javascript

- [Select Objects from HTML](#select-objects-from-html)

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
