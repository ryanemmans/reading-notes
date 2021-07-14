# CLASS 02 NOTES - Basics of HTML, CSS, & JavaScript

## **From Jon Duckett's "HTML&CSS"**

- *Code examples referenced from the text*

- - -

## ***Chapter 2 - Text***

HTML elements are used to describe the **structure** of the page (e.g. headings, subheadings, paragraphs).

### **Structural markup**

- Elements that can describe both headings and paragraphs

Headings - `<h1>` (main heading / largest), `<h2>` (sub-headings), down to `<h6>` (smallest/lowest level)

Paragraphs `<p>` - bodies of text, one of more sentences

- Bold `<b>`, italic `<i>` - for emphasis
- `<sup>` - superscript element - raises text (such as number suffixes or exponents)
- `<sub>` - subscript element - lowers text (such as footnotes or chemical formulas)

White space (tabs and spacing) is used to make code easier to read.

`<br />` - line break, `<hr />` - horizontal rule

### **Semantic markup**

- Extra information such as where emphasis is placed
  - `<strong>` - indicates strong importance
  - `<em>`- indicates emphasis that subtly changes meaning
  - `<blockquote>` - longer quotes (`<p>` can be used inside)
  - `<q>` - shorter quotes
  - `<abbr>` - abbreviation or acronym (`title` attribute specifies full term)
  - `<cite>`- citations, such as books, films, research papers
  - `<dfn>` - defining instance of a new term
  - `<address>` - author contact details
  - `<ins>` & `<del>` - insert and delete conent
  - `<s>` - strikethrough, no longer accurate or relevant info, but not deleted

- - -

## ***Chapter 10 - Introducing CSS***

CSS treats each HTML element as if it appears inside its own box

- Block and inline elements
- Uses rules to indicate how that element should look

Rules are made up of selectors and declarations

- ***Selectors*** specify which elements the rules apply to (ex: `p`)
- ***Declarations*** indicate what these elements should look like (ex: `{font-family: Arial;}`)

Declarations are made up of two parts:

1. ***Properties*** of the element you want to change (ex: `font-family`)
2. The ***Values*** of those properties. (ex: `Arial`)

CSS rules usually appear in a separate document (external)

```html
<head>
  <title>Using External CSS</title>
  <link href="css/styles.css" type="text/css" rel="stylesheet" />
</head>
```

CSS may also appear within an HTML page - internal (head) or inline (body)

```html
<head>
  <title>Using Internal CSS</title>
    <style type="text/css">
      body {
        font-family: arial;
        background-color: rgb(185,179,175);}
      h1 {
        color: rgb(255,255,255);}
    </style>
</head>
```

### Benefits of external style sheets

- can be applied to entire site, faster loading, ***much easier*** maintenance for multiple pages, cleaner code

Different types of selectors allow you to target your rules at different elements

- Universal (`*`), type (`name`), class (`.`), id (`#`), child (`>`), descendant (`name1 name2`), adjacent sibling (`+`), general sibling (`~`)
- **SEE PAGE 238** for detailed breakdown

More specific rules take precedence over more general ones

- Properties can also be designated importance (`!important`)
- Properties and their values can be inherited by child elements

- - -

## **From Jon Duckett's "JavaScript&JQuery"**

- *Code examples referenced from the text*

- - -

## ***Chapter 2 - Basic JavaScript Introductions***

### **Statements**

A script is made up of a series of statements

- Each statement is like a **step** in a recipe
  - Each one starts on a new line, ends with `;` (indicates when step is over)
- Curly braces `{ }` that surround statements indicate code blocks
  - can be used to group multiple statements
    - makes code more organized and readable

Scripts contain very precise instructions

- Ex: value must be remembered before creating a calculation using that value

Comments should be used to explain what your code does

- `/*`. . .`*/` multi line
- `//` single line

### Variables temporarily store pieces of info (or data) used in a script

- Data stored can change (or *VARY*) each time a script runs
- Variables must be declared (or announced that you want to you them)
  - Ex: `var quanity;` where `var` is the *keyword* and `quantity` is the name (or identifier)
  - more than one word in the name uses camelCase (note lower and uppercase)
- Once a variable is created, you can assign it value.
  - Ex: `quantity = 3;`

### JavaScript distinguishes between different data types that variables can store

- numeric (0-9 - no quotes)
- strings (text - single or double quotes)
  - backslash `\` can be used to *escape* quotation characters
- and Boolean values (`true` or `false` - no quotes)

### Shorthand can be used in a number of ways to create variables

```javascript
var price = 5;
var quantity =14;
var total =price * quantity;
```

```javascript
var price, quantity, total ; price =5;
quantity= 14;
total =price * quantity;
```

```javascript
var price var total
5, quantity = 14; price * quantity;
```

```javascript
// Write total into the element with id of cost
var el =document.getElementByld('cost'); el.textContent ='$' +total;
```

Variable values can be changed later in the script using only the name, the keyword (in this case `var`) is not needed. Ex:

```javascript
var inStock;
var shipping;

inStock = true;
shipping = false;

/* Some other processing might go here and, as a result, the script might need to change these values */

inStock = false;
shipping =true;
```

### Rules for Naming Variables

1. must begin with letter, (`$`), or (`_`)
2. cannot contain (`-`) or (`.`)
3. cannot use keywords (such as `var`) or reserved words
4. case sensitive! Bad practice to have 2 variables with same name but different cases.
5. use a name that describes the info being stored
6. use camelCase for multiple words (ex: `firstName` instead of `firstname`). No dashes!

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

### Expressions evaluate (or result) into a single value. There are two types

1. Just assign a value to a variable
    - ex: `var color = 'beige';`
2. Use two or more values to return a single value
    - ex: `var area = 3 * 2;`

Expressions rely on ***operators*** to calculate a value.

- Assignment - assign value
- Arithmetic - perform basic math
- String - combine two strings (`+`)
- Comparison - compare two values, return `true` or `false`
- Logical - combine expressions, return `true` or `false`

- - -

## ***Chapter 4 - Decisions & Loops***

### **Conditional statements** allow your code to make decisions about what to do next

- Based on `if...else` statements
- The code can take one of two different paths, each made up of different sets of tasks
  - You must write different code for each situation
  - If the **condition** returns `true` you take one path, `false` takes the other
    - determined through the use of *comparison operators*

### Comparison operators are used to compare two operands

- `(===, !==, ==, !=, <, >, <=, =>)`
- structure example; `(score >= pass)`

Operands do not need to be single values or variable names. They can also be expressions (which evaluate into a single value)

- ex: `((score1 + score2) > (highScore1 + highScore2))`

Logical operators allow you to combine more than one set of comparison operators.

- `&&` logical and, `||` logical or, `!` logical not
- ex: `((5 < 2>) && (2 >= 3))`
  - both expressions return `false`, the logical `&&` operator evaluates entire expression to be `false`

`if` statements evaluate (or check) a condition

- if `true`, any statements in subsequent code block are executed

```javascript
if (score >= 50) {
   congratulate();
}
```


`if...else` statements also check a condition

- if `true`, first code block is executed
- if `false`, second code block is run instead

```javascript
if (score >= 50) {
   congratulate();
}
else {
   encourage();
}
```

`switch` statements allow you to compare a value against possible outcomes

- They start with a variable called the **switch value**
- They also provide default option if no cases match
- Provides better performance than multiple `if` statements

[back](../README.md)
