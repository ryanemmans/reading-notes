# CLASS 07 NOTES - Object-Oriented Programming, HTML Tables

## **Domain Modeling**

Domain Modeling - the process of creating a conceptual model in code for a specific problem

- Model describes various entities, their attributes and behaviors, and constraints that govern the problem domain

Entity - **object-oriented** model

Domain model can verify and validate specific problem

- communication tool - defines a useful vocab

### Define a Constructor and Initialize Properties

Same properties between many objects - use a constructor function

- defined using a **function expression**

Storing data within properties ensures any newly created object can access that data later

Objects are then **instantiated** (or created) and then properties are **initialized**

- Object is stored in a variable for later use

### Generate Random Numbers

Methods can be added to a constructor function's prototype and then located

When a prototype is shared between two or more objects, those objects execute the same code when the `generateRandom()` method is called

### Calculate Daily Likes

Viewers times percentage

- 2 variables are defined

`Math.round` can round these variables to the near integer

### Calculate Weekly Likes

Method on the prototype is assigned a function with no parameters

- declares a `total` variable that's initialized to `0`

### Summary

Single entity with many instances

- Build self-contained objects with the same attributes and behaviors.

Model attributes with a constructor function

- Defines and initializes properties.

Model behaviors with small methods

Create instances using the `new` keyword

- followed by call to constructor function.

Store the new object in a variable

- able to access its properties and methods from outside.

Use the this variable within methods

- Access object's properties and methods from inside.

- - -

## **From Jon Duckett's "HTML&CSS"**

- *Code examples referenced from the text*

- - -

## ***Chapter 5 - Tables***

### A table represents information in grid format

- Such as sports results, stock reports, timetables

The `<table>` element is used to add tables to a web page

Drawn out row by row. Each row is created with the `<tr>` element

Inside each row there are a number of cells represented by the `<td>` element

```html
<table>
  <tr>
    <td>15</td>
    <td>15</td>
    <td>30</td>
  </tr>
  <tr>
    <td>45</td>
    <td>60</td>
    <td>45</td>
  </tr>
  <tr>
    <td>60</td>
    <td>90</td>
    <td>90</td>
  </tr>
</table>
```

Or `<th>` if it is a header

- uses `scope` attribute to indicate column or row

You can make cells of a table span more than one row or column using the `rowspan` and `colspan` atttributes

For long tables you can split the table into a `<thead>`, `<tbody>`, and `<tfoot>`

- Similar to the body structure of an HTML page

Old code utilizes width, spacing, border, and background

- - -

## **From Jon Duckett's "JavaScript&JQuery"**

- *Code examples referenced from the text*

- - -

## ***Chapter 3 - Functions, Methods, and Objects***

Web browsers implement objects that represent both the browser window and the document loaded into the browser window.

`new` keyword and object constructor create a blank object

- Properties and methods can then be added to the object

Property values can be updated using dot notation or square brackets

- Literal or Constructor notation
- use `delete` keyword to delete

Object constructors can use a function as a **template** for creating objects

- create **instances** of the object
-`new` keyword followed by call to function creates new object
  - properties are given as arguments

Keyword `this` is commonly used inside functions and objects

- refers to one object usually inside where the function operates

Arrays or objects can be used to group a set of related values

To access items via proeprty name or key, use an object

- keys must be unique

If item order is important, use an array

### Arrays are a special type of object

- key for each value is its index number

Arrays and Objects can be combined to create complex data structures

- Objects can hold arrays

### Three Groups of Built-in Objects

- Browser Object Model - Window Object
- Document Object Model - Document Object
- Global JavaScript Objects
  - `String`, `Number`, `Math`, `Date`, `Boolean`, `Regex`
- Their properties and methods offer functionality that help you write scripts.

To work with dates, you create and instance of the **Date** object

- specify when you want it to represent

[back](../README.md)
