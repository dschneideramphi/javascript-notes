# Computer Apps II - Introduction to Javascript

- [Select Objects from HTML](#select-objects-from-html)
- [Events](#events)
- [Apply Classes with Javascript](#apply-classes-with-javascript)
- [Change Text On A Website](#change-text-on-a-website)
- [Prompt The User](#prompt-the-user)
- [Use Variables In Text](#use-variables-in-text)

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

### Practice Repositories

[Lightbulb Selector](https://github.com/upperlinecode/lightbulb-selector-template)

## Apply Classes With Javascript

When you have a class defined in a CSS file, use the following methods to apply that style to HTML elements:

- `.classList.add()`
- `.classList.remove()`
- `.classList.toggle()`

**CSS**
```CSS
.red {
  background-color: red;
}
.blue {
  background-color: blue;
}
```

**Javascript**
```javascript
redBtn.addEventListener("click", (e) => {
    divElt.classList.remove("blue");
    divElt.classList.add("red");
});

blueBtn.addEventListener("click", (e) => {
    divElt.classList.remove("red");
    divElt.classList.add("blue");
});
```

### Pro-Tips
- Use `toggle` if you want a button to switch a class on & off
- Use `add` and `remove` if you only want one class applied at a time
- Make sure `classList` has a capital L

### Practice Repositories

[Class Button Lab](https://github.com/upperlinecode/class-button-js-lab)

## Change Text On A Website

Use `.innerHTML` to change the text that is between an opening an closing HTML tag.

**Initial HTML**

```HTML
<div>
  My Name Is <span id="name">Alice</span>
</div>
```

**Javascript**
```javascript
let nameElt = document.querySelector("#name");
nameElt.innerHTML = `Bob`;
```

**Updated HTML**
```HTML
<div>
  My Name Is <span id="name">Bob</span>
</div>
```

### Pro-Tips
- use back-ticks rather than quotes (as above)
- You can include other HTML as part of the `innerHTML` code

### Practice Repositories
- [Animal Selector](https://github.com/dschneideramphi/ahs-animal-selector)

# Prompt The User

Use `let ____ = prompt()` to ask the user for information. The result will be stored in a variable.

**Javascript**

```javascript
let color = prompt("What is your favorite color?");
let divElt = document.querySelector("#bigDiv");
divElt.style.background = color;
```

**The Result:** This should change the background color of a div to whatever the user types in

### Pro-Tips

- Even if the user types a number, the computer thinks it's a string, so trying to perform math takes some extra steps

### Practice Repositories

- [Choose-Your-Own Newspaper](https://github.com/dschneideramphi/ahs-design-newspaper)

# Use Variables In Text

Using back-ticks, you can use `${___}` to insert a variable in the middle of a string. This is useful when using `.innerHTML` to create a full sentence rather than piece by piece

**Javascript**
```javascript
let name = "Schneider";
let hobby = "Origami";
console.log(`My name is ${name} and I like ${hobby}`);
name = "Rossi";
hobby = "Football";
console.log(`My name is ${name} and I like ${hobby}`);
```

**Result**
> My name is Schneider and I like Origami

> My name is Rossi and I like Football

### Practice Repositories

- [Mad Lib](https://github.com/dschneideramphi/ahs-mad-lib)
