# CLASS 03 NOTES - HTML Lists, CSS Boxes, JavaScript Control Flow

## **From Jon Duckett's "HTML&CSS"**

- *Code examples referenced from the text*

- - -

## ***Chapter 3 - Lists***

### There are three types of HTML lists

- Ordered - `<ol>` - numbers, `<li>` is used for list item
- Unordered - `<ul>`- bullets, `<li>` is used for list item
- Definition - `<dl>` - define terminology
  - `<dt>` - term being defined
  - `<dd>` - contains the definition

### Lists can be nested inside one another

- Here is an example:

```html
<ul>
  <li>Mousses</li>
  <li>Pastries
    <ul>
      <li>Croissant</li>
      <li>Mille-feuille</li>
      <li>Palmier</li>
      <li>Profiterole</li>
    </ul>
  </li>
  <li>Tarts</li>
</ul>
```

- - -

## ***Chapter 13 - Boxes***

### CSS treats each HTML element as if it has its own box

You can use CSS to control the dimensions of a box

- `width` and `height`
- Limiting width - `min-width, max-width`
- Limiting height - `min-height, max-height
- `overflow: hidden; overflow: scroll;`

You can also control the borders, margin, and padding for each box with CSS

- Top, Right, Bottom, Left can all be specified for all of these
  - **Border** seperates the edge of one box from another
    - `width, style, color`
    - Shorthand can also be used
      - `border: 3px dotted #0088dd;}`
  - **Margin** is space outside of border
  - **Padding** is space between border and content within

Block-level boxes can be made into inline boxes, and vice versa

- `display: inline;` - block acts like inline
- `display: block;` - inline acts like block
- `display: inline-block;` - block level flows like inline element, while retaining other features of a block level element

It is possible to hide elements using the display and visibility properties
- `display: none;`
- `visibility: hidden;`
- `visibility: visible;`

Legibility can be improved by controlling the width of boxes containing text and the leading

CSS3 has introduced the ability to create image borders and rounded borders
- `box-shadow: 5px 5px 5px 5px #777777;`
  - horizontal offset, vertical offset, blur distance, spread
- `border-radius:`
- Elliptical shapes can also be created

- - -

## **From Jon Duckett's "JavaScript&JQuery"**

- *Code examples referenced from the text*

- - -

## ***Chapter 2 Review - Basic JavaScript Instructions***

### Arrays

Arrays are special types of variables that store ***lists*** of values (or multiple pieces of *related* information)

- **Array Literal** technique - values are assigned inside square brackets `[ ]` using commas (`,`) to separate each

```javascript
var colors;
colors ['white', 'black', 'custom'];

var el document.getElementByld('colors');
el.textContent =colors[O];
```

- **Array Constructor** technique - values specified in parentheses `( )`, again separated by comma

```javascript
var colors
new Array('white',
          'black',
          'custom');

var el =document.getElementByid('colors');
el.innerHTML =colors.item(O);
```

Numbering in these lists start at zero (not one)

- each item is given a number called an **index** which allows you to access them and change values

- - -

## ***Chapter 4 - Decisions & Loops (continued)***

### Switch Statements

`switch` statements allow you to compare a value against possible outcomes

- They start with a variable called the **switch value**
- They also provide default option if no cases match
- Provides better performance than multiple `if` statements
- If a match is found, that code is run
  - then the `break` statements stops it from running

Date types can be coerced from one type to another

- Type coercion can lead to unexpected values
  - use strict equals operators `===` and `!==` rather than `==` and `!=` to check that value and data types match

All values evaluate to either `truthy` or `falsy`

- treated *as if* they are `true` or `false`
- `falsy` values can also be treated as the number 0
- `truthy` values can also be treated as the number 1
- Object or array is usually considered `truthy` as well

Logical operators are processed left to right

- They stop as soon as they have a result, but return the value that stopped the processing (not necessarily `true` or `false`)

There are three types of loop. Each repeats a set of statements

- `for` - run code specific number of times (most common)
  - conditiona is usually a counter

```javascript
var scores = [24, 32, 17];      // Array of scores
var arrayLength = scores.length;// Items in array
var roundNumber = 0;            // Current round
var msg = '';                   // Message

// Loop through the items in the array
for (var i = 0; i < arrayLength; i++) {

  // Arrays are zero based (so 0 is round 1)
  // Add 1 to the current round
  roundNumber = (i + 1);

  // Write the current round to message
  msg += 'Round ' + roundNumber + ': ';

  // Get the score from the scores array
  msg += scores[i] + '<br />';
}

document.getElementById('answer').innerHTML = msg;
```

- `while` - when you don't know how many times code should run
  - code will continue to loop until condition is `true`

```javascript
var i = 1;       // Set counter to 1
var msg = '';    // Message

// Store 5 times table in a variable
while (i < 10) {
  msg += i + ' x 5 = ' + (i * 5) + '<br />';
  i++;
}

document.getElementById('answer').innerHTML = msg;
```

- `do...while` - similar to `while`
  - will always run statements at least once, even if condition is `false`

```javascript
var i = 1;       // Set counter to 1
var msg = '';    // Message

// Store 5 times table in a variable
do {
  msg += i + ' x 5 = ' + (i * 5) + '<br />';
  i++;
} while (i < 1); 
// Note how this is already 1 and it still runs

document.getElementById('answer').innerHTML = msg;
```

### Loop Counters

Initilization `var i = 0;`

Condition `i <10;`

Update `i++`

```javascript
var i;
for (i = 0; i <10; i++) {
  // Code goes here
}
```

1. The loop is run, variable `i` (the counter) is assigned a value of zero
2. Condition is checked everytime loop is run. Is `i` less than `10`?
3. Then code between curly brackets is run
4. `i` can be used inside loop to write a number to the page
5. When statements finish, `i` increments by 1 (`++`)
6. When condition is no longer true, the loop ends and script moves to next line of code

**`break`** - termination of loop - go to next statement outside of loop

**`continue`** - ...and check condition again - if `true`, it runs again

[back](README.md)
