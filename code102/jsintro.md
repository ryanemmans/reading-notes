# JAVASCRIPT:

- Programming language that allows you to implement complex things on web pages
- Best known as the scripting language for web pages
- Lightweight, interpreted or “just-in-time” compiled language with first-class functions (treated like any other variable)
- A function can be passed as an argument to other functions
  - Can be returned by another function
  - Can be assigned as a value to a variable
- Displays things such as updates, interactivity, animation, and more
- Can also be used on non-browser environments such as Node.js, Apache CouchDB, and Adobe Acrobat
- Runs on client side of web - used to design and program page behavior in response to event occurrence
- Not to be confused with Java!

## ***Javascript is dynamic, multi-paradigm, single-threaded***

- Runtime object construction, variable parameter lists, function variables, dynamic script creation object introspection, and source code recovery
- Procedural - contains a series of computational steps to be carried out

## Javascript supports:

- Prototype-based object construction
- Object-oriented styles
- Imperative styles
- Declarative styles (e.g. functional programming)

Objects are created by attaching methods and properties to them *at run time*

- Once constructed, an object can be used as a blueprint or prototype for creating similar objects

- Variables are containers for storing data (values)
- 3 ways to declare a variable: >> *var, let, or const*
  - `var` is a global variable - you can use it anywhere in your code
  - `let` is scoped to where you create it

## All variables need unique names, or *identifiers*

- They can contain letters, digits, underscores, and dollar signs
- Case sensitive, cannot begin with a digit
- Equal sign is an assignment operator
- `==` is “equal to”

## Javascript Data Types:

- Text values are called strings - written inside double or single quotes.
- Numbers are written without quotes.

1. Declare (create) variable
2. Name variable
3. Assign (give) variable value - use equal sign. Ex: `var carName = "Volvo";`
    - strings (text) in quotes, numbers no quotes! 
4. Output value to HTML with an “id” (DOM - document object model)

***It's a good programming practice to declare all variables at the beginning of a script.***

- You can declare multiple variables in one statement
- A declaration can span multiple lines

Variables have a value of “undefined” until given actual value. Ex: `var carName;`

- Value can be calculated, or later provided by user input
- If you re-declare a variable, it will not lose it’s value

You can also add strings, but strings will be concatenated (linked in a series)
If you put a number in quotes, the rest of the numbers will be treated as strings, and concatenated (linked).

- Ex: `var x = "5" + 2 + 3;` x = 523
- `var x = 5 + 2 + 3;` x = 10
- `var x = 5 + 2 + “3”;` x = 73
- **Quotes remove numeric properties and present them as text**

Javascript treats *dollar sign* as a letter, therefore variable names can begin with dollar sign

- Often used as an alias for main function in a library

Javascript also treats *underscore* as a letter, therefore variable names can begin with underscore

- Often used as an alias for private (or hidden) variables

[back](../README.md)
