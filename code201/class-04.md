# CLASS 04 NOTES - HTML Links, Intro to CSS Layout, and JavaScript Functions

## **From Jon Duckett's "HTML&CSS"**

- *Code examples referenced from the text*

- - -

## ***Chapter 4 - Links***

### Links enable the very idea of browsing and surfing the web

- they are the defining feature of the web

Links are created using the `<a>` element

- uses the `href` attribute` to indicate the page you are linking to

`<a href="http://www.imdb.com">IMDB</a>`

Use relative links to pages within your site rather than qualified URLs

- shorthand version - domain name not needed
- URL stands for '**U**niform **R**esource **L**ocator'

### Directory Structure

- Folder Relationships - Grandparent, Parent, Child, Grandchild
- `index.html` will always be the Homepage

Folders must be specified when using relative links

- `<a href="movies/dvd/reviews.html">`

You can create links to open email programs with an email address in the "to" field

- `<a href="mailto:jon@example.org">Email Jon</a>`

Opening links in a new window uses `target="_blank"`inside `<a>` tag

You can use the `id` (`#`) attribute to link directly to elements *within* a page

- `<a href="#interlude">Interlude</a>` would link to `<h2 id="interlude">Interlude</h2>` further down the page
- `<a href="http:/www.htmlandcssbookcom/ #bottom">` would link to a specific part of a ***different*** page

- - -

## ***Chapter 15 - Layout***

### How to control where each element sits on a page, making attractive page layouts

### Positioning Elements

CSS treats each HTML element as if it is in its own box.

- Either a block-level box or an inline box
  - Block-level - start on new line, act as main building blocks
  - Inline - flow between surrounding text
- Boxes can be separated with borders, margins, padding, and background colors

Outer Box is **containing** or **parent** element of element inside it

`<div>` often used as containing elements to group together sections of a page

Browsers display pages in *normal flow* unless you specify relative, absolute, or fixed positioning

- Relative - shifts element to top, right, bottom, or left of where it *would have* been placed
- Absolute - does not affect surrounding elements.
  - Moves as users scroll up and down the page.
- Fixed - type of absolute, does not move when scrolling

`float` property moves content to left or right of page

```css
p {
  width: 230px;
  float: left;
}
```

Float can be used to create multi-column layouts

- placing elements side by side
- items require defined width

```css
.column1of2 {
  float: left;
  width: 620px;
  margin: 10px;
}
.column2of2 {
  float: left;
  width: 300px;
  margin: 10px;
}
```

`z-index` controls order of overlapping boxes (which is on top)

```css
h1 {
  position: fixed;
  z-index: 10;
}
```

The clear property allows you to say that no element (within the same containing element) should touch the left or right-hand sides of a box.

- `left`, `right`, `both`, `none`

```css
.clear {
  clear: left;
}
```

Pages are kept within 960-1000 pixels wide

- indicate what the site is about within top 600 pixels
  - this demonstrates the page's relevance without scrolling
  - accounts for different screen sizes and resolutions

Fixed width layout designs

- Do not change size as browser window increases or descreases
- Measurements tend to be given in pixels.

Liquid layout designs

- Stretch and contract
- Tend to use percentages.

Grids help create professional and flexible designs

CSS Frameworks provide rules for common tasks

You can include multiple CSS files in one page

- In CSS:

```css
@import url("tables.css");
@import url("typography.css");
```

OR in HTML:

```html
<head>
<title>Multiple Style Sheets - Link</title> <link rel="stylesheet" type="text/css"
      href="css/site.css" />
    <link rel="stylesheet" type="text/css"
      href="css/tables.css" />
    <link rel="stylesheet" type="text/css"
        href="css/typography.css" />
  </head>
```

- - -

## **From Jon Duckett's "JavaScript&JQuery"**

- *Code examples referenced from the text*

- - -

## ***Chapter 3 - Functions, Methods, & Objects***

### Functions allow you to group a set of related statements together to perform a specific task

Functions can take parameters and may return a value

- Parameters are information required for a function to do its job

```javascript
var msg = 'Sign up to receive our newsletter!';
function updateMessage() {
  var el = document.getElementByld('message'};
  el .textContent = msg;
}
updateMessage();
```

### Declaring a Function

```javascript
function sayHello() {
  document.write('Hello!');
}
```

- `function` is keyword
- `sayHello` is name
- `{document.write('Hello!');}` is code block.

Calling a function - `sayHello();`

### Function Parameters (requiring information)

- In this case, width and height

```javascript
function getArea(width, height) {
  return width * height;
}
```

### The following sections will be updated soon

- Calling Functions
- Getting a single or multiple values out of a function
- Function Expression
- Variable Scope

- - -

## ***6 Reason For Pair Programming***

### How does pair programming work?

- The Driver is the only one typing and handles the "mechanics" of coding
- The navigator uses their words to guide the driver

### Why pair program?

Four fundamental skills

1. Listening
2. Speaking
3. Reading
4. Writing

### 1. Greater Efficiency

- Two programmers may come to a solution faster than one programmer on their own.
- Enhances technical skills, communication, and enjoyability

### 2. Engaged Collaboration

- Accountability hinders procrastination
- Knowing when to ask for help

### 3. Learning From Fellow Students

- Different skill sets

### 4. Social Skills

- Interpersonal skills
- Long term career impacts

### 5. Job Interview Readiness

- Gives companies an idea of how applicants will fit into teams

### 6. Work Environment Readiness

- Grads can hit the ground running

[back](../README.md)
