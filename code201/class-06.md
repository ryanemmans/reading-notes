# CLASS 06 NOTES - Problem Domain, Objects, and the DOM

## **Understanding the Problem Domain Is The Hardest Part of Programming**

- Learning a new technology
- Naming things
- Testing your code
- Debugging
- Fixing bugs
- Making software maintainable

### A Familiar Problem

When applications are simple and easy to understand, the focus is taken off of the problem domain and instead put on the technology

By creating a familiar problem domain

- both teaching a new technology and the viewer learning the technology become much easier

### Why problem domains are hard

Writing code is similar to putting together a jigsaw puzzle

- with the purpose of building components that we have taken out of the "bigger picture" of the problem domain

We are often not given complete information needed to understand problem domain

### Programming is easy if you understand the problem domain

When the problem domain is clear and easy to learn, code can be written easily as well

### What can you do about it?

Make the problem domain easier

- Cut out cases and narrow your focus to a particular part of a problem

Get better at understanding it before expanding it
- learn it inside and and out before trying to solve it
- much more expensive and time consuming to do things over and over
- instead do things right the first time

- - -

## **From Jon Duckett's "JavaScript&JQuery"**

- *Code examples referenced from the text*

- - -

## ***Chapter 3 - Object Literals***

In an object, variables are known as properties of the object

- Value of property can be string, number, Boolean, array or another object

- Functions are known as methods of the object
  - Value is always a method

Object names are called a ***key*** (name/value pair)

- Used to access corresponding values
- Cannot have 2 keys with the same name

### Objects are created using literal notation

```js
var hotel = {
  name: 'Quay',
  rooms: 40,
  booked: 25,
  checkAvailability: function() {
    return this.rooms - this.booked;
  }
};
```

### Access properties or methods of an object using dot notation

- `var hotelName = hotel.name;`

Or square brackets

- `var hotelName = hotel['name'];`

- - -

## ***Chapter 5 - Document Object Model***

### DOM specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window

The browswer represents the page using a DOM tree

Dom trees have four types of nodes

- document nodes - represents entire page
- element nodes - `<h1>` `<p>`
- attribute nodes - *part* of the element
- text nodes - cannot have children

You can select element nodes by the `id` or `class` attributes, by tag name, or using CSS selector syntax

SEE PAGES 188-189 on accessing and working with elements

### Methods that return single element node

- `getElementById('id')`
- `querySelector('css selector')`

Whenever a DOM query can return more than one node, it will always return a `NodeList`

- `getElementsByClassName('class')`
- `getElementsByTagName('tagName')`
- `querySelectorAll('css selector')`

### Selecting an element from a node list

1. The `item()` method
    - uses length property

    ```js
    var elements = document.getElementsByClassName('hot')
    if (elements.length>= 1) {
      var firstltem = elements.item(O);
    }
    ```
2. Array syntax - preferred for speed
    ```js
    var elements = document.getElementByClassName('hot');
    if (elements.length >= 1) {
      var firstItem = elements[0];
    }
    ```

When you have a NodeList, you can loop through each node in the collection and apply the same statements to each - SEE PAGE 206 for example

### Traversing the DOM

- When you have an element node, you can select another element in relation to it using properties

  - `parentNode`
  - `previousSibling`
  - `nextSibling`
  - `firstChild`
  - `lastChild`

### How to get/update element content

- Navigate to the text nodes
- Work with the containing element

An element node can contain multiple text nodes and child elements that are siblings of each other

- When you select a text node, you can retrieve or amend the content of it using the `nodeValue` property

From an element node, you can access and update its content using properties such as `textContent`, `innerText`, and `innerHTML` or using DOM manipulation techniques

- DOM manipulation easily targets individual nodes in DOM tree
- `innerHTML` is better suited to updating entire fragments
  - text and markup can be updated
  
Elements can also be added to DOM tree...

- `createElement()`
- `createTextNode()`
- `appendChild`

... Or removed

- element is stored in variable
- its parent is stored in a variable
- `removeChild()` removes element from its parent

Techniques for adding HTML to a webpage, all come with advantages and disadvantages

- `document.write()`
- `element.innerHTML`
- DOM Manipulation

### Cross-site scripting (XSS) attacks

- attackers could gain access to user account if `innerHTML` is used to add HTML
- use input validation for defense

### Attribute Nodes

Once you have an element node, you can use other properties and methods on that element node to access and change its attributes

- attribute values can be obtained
- attributes can be created and their values changed
- attributes can be removed

In older browsers, implementation of the DOM is inconsistent

- popular reason for using JQuery

Browsers offer tools for viewing the DOM tree