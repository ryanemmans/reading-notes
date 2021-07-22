# CLASS 09 NOTES - Forms and JavaScript Events

## **From Jon Duckett's "HTML&CSS"**

- *Code examples referenced from the text*

- - -

## ***Chapter 7 - Forms***

Forms are used to collect information from visitors

- Live inside a `<form>` element
- Examples are a search box or an application

## Form Controls

Adding Text

- Text input (single-line)
- Password input - masks characters
- Text area (multi-line)

Making Choices

- Radio buttons
- Checkboxes
- Drop-down boxes

Submitting Forms

- Submit buttons
- Image buttons

Uploading Files

Information from a form is sent in name/value pairs

- The text the user types in / values of options they select are sent to the server
- The server processes the information using a language such as PHP, C#, VB.net, or Java
  - Can also be stored in a database
- Server creates new page to send back to browser based on information received.

## Form Structure

`action` - value is URL for page on server that will receive in the form when it is submitted

`method` - `get` or `post`

- `get` - values from forms are added to the end of the URL specified in `action` attribute
  - used for short forms or just retrieving data from web server
- `post` - values are sent in what known as HTTP headers
  - used if form allows users to upload a file
  - is very long
  - contains sensitive data like passwords
  - or adds/deletes info to/from a database

`get` is used if `method` is not used

`id` - value is used to identify form distinctly from other elements on page

- often used by scripts such as those that check to have entered info into fields that require values

- - -

### Text Input

- `type="text"`, `name`, `size`, `maxlength`

### Password Input

- `type="password"`, `name`, `size`, `maxlength`

### Radio Button

- `type="radio"`, `name`, `value`, `checked`

### Checkbox

- `type="checkbox"`, `name`, `value`, `checked`

### Drop Down List Box

- `<select>` - `name`
- `<option>` - `value`, `selected`

### Multiple Select Box

- `<select>` - `size`, `multiple`

### File Input Box

- `<input>` - `type="file"`

### Submit Button

- `<input>` - `type="submit"`, `name`, `value`

### Image Button

- `<input>` - `type="image"`

### Button & Hidden Controls

- `<button>`, `<input>` - `type="hidden"`

### Labeling Form Controls

- `<label>` - `for`
  - Above or to the left - text inputs, text areas, select boxes, file uploads
  - To the right - individual checkboxes or radio buttons

### Grouping Form Elements

- `<fieldset>`, `<legend>`

HTML5 introduces new form elements which make it easier for visitors to fill in forms

- Form validation
- Date input
  - `<input>` - `type="date"`
- Email & URL input
  - `<input>` - `type="email"`, `type="url"`
- Search input
  - `<input>`, `type="search"`, `placeholder`

- - -

## ***Chapter 14 - Lists, Tables, and Forms***

### There are several CSS properties that are specifically used to control the appearance of lists, tables, and forms

List markers can be given different appearances using the `list-style-type` and `list-style` image properties

- can use bullet point styles (`type`) or images for bullets (`image`)

`list-style-position` - `outside` or `inside`

`list-style` can be used for shorthand

- `list-style: inside circle;`

Table cells can have different borders and spacing in different browsers

- there are properties you can use to control them and make them more consistent

Border on Empty Cells - `show`, `hide`, `inherit`

Gaps Between Cells - `border-spacing`, `border-collapse`

Text inputs, buttons, fieldsets, and legends can all be styled with CSS

Forms are easier to use if the form controls are vertically aligned using CSS

- `float` can be used

Cursors can also be styled

Forms benefit from styles that make them feel more interactive

- - -

## **From Jon Duckett's "JavaScript&JQuery"**

- *Code examples referenced from the text*

- - -

## ***Chapter 6 - Events***

Events are the browser's way of indicating when something has happened

- such as when a page has finished loading or a button has been clicked

### Interactions Create Events - Events Trigger Code - Code Responds to Users

There can be UI Events, Keyboard Events, and Mouse Events - SEE PAGE 246

Events fire or are raised. They also trigger scripts

- Focus, Form, Mutation (when the DOM structure has been changed by a script)

1. Select Element
2. Specify Event
3. Call Code

Binding - the process of stating which event you are waiting to happen

- which element you are waiting for that event to happen upon

There are 3 ways to bind an event to an element

- HTML event handlers **(Do Not Use)**
- Traditional DOM event handlers
  - `element.onevent = functionName;`
  - ^ element, event, code ^
- DOM Level 2 event listeners

Event listeners are made up of an element and a method

- within the method is the event, code, and event flow

Parameters can be used with event handlers and listeners

### Event Flow
HTML elements nest inside other elements.

- If you hover or click on a link, you will also be hovering or clicking on its parent elements.
- **Event Bubbling** - starts at most specific node and *flows outwards*
- **Event Capturing** - starts at least specific node and *flows inwards*

Flow matters when your code has even handlers on an element AND one of its ancestor or descendant elements

When an event occurs, the `event` object tells you info about the event AND the element it happended on

- Event listeners can be used with the event object

When an event occurs on an element, it can trigger a JavaScript function.

- When this function then changes the web in some way, it feels interactive because it has responded to the user

You can use event delegation to monitor for events that happen on all of the children of an element

- works with new elements
- solves limitations with `this` keyword
- simplifies your code

Changing default behavior

- `preventDefault()`
- `stopPropogation()`

When calling a function, the `event` object's `target` property is best way to determine which element event occurred on

- `this` keyword and parameters can be used

The most commonly used events are W3C DOM events

- there are others in HTML5 spec as well as browser-specific events (BOM)

User Interface (UI) events occur as a result of interaction with browser window rather than HTML page contained within it

- e.g., page loading, window resizing

Focus & Blur Events

- Links and forms can gain focus, causing the focus and blur events to fire

The `event` object can tell you where the curor was positioned when an event was triggered

- Screen, page, client

[back](../README.md)
