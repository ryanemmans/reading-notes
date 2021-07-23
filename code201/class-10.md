# CLASS 10 NOTES - Debugging

## **From Jon Duckett's "JavaScript&JQuery"**

- *Code examples referenced from the text*

- - -

## ***Chapter 10 - Error Handling & Debugging***

### Programming is like problem solving.

- You are given a puzzle that you must solve AND create the instructions that allow the *computer* to also solve it.

## Execution contexts have two stages.

- Global Context - code that is in the script, but not in the function
  - Only one per page.
- Function Context - code that is being run within a function.
  - Each function has it's own context

Variable Scope

- Global Scope - variables outside of functions, not use `var` to create a variable
- Function Level Scope - variable declared within a function can only be used within that function

## Stack

When a statement needs data from another function, it **stacks** (or piles) the new function on top of the current task

- Each time a new item is added to the stack, it creates a new execution context
- If a function gets called a second time, the variables can have different values

If you understand execution contexts and stacks, you are more than likely to find the error in your code.

Two phases of activity each time a script enters a new execution context

1. Prepare
    - New scope is created
    - Variables, functions and arguments are created
    - Value of `this` keyword is determined

2. Execute
    - Assign values to variables
    - Reference functions and run their code
    - Execute statements

Preparation phase - taking all variables and functions and ***hoisting*** them to the top of the execution context

`variables` object applied to execution context

- Details of all variables, functions, and parameters

Lexical Scope - linked to the object a function is defined *within*

If JavaScript generates an error, it throws an **exception**

- Interpreter stops and looks for exception handling code

## Error Objects

- can help you find where your mistakes are - SEE PAGE 459 for examples

JavaScript has 7 different types of errors

- Each creates its own error object
  - Can tell you its line number and gives a description of the error

Debugging is the process of finding errors.

- Involves a process of deduction and tracking down the source of an error
  - eliminating potential cuases

Where is the problem?

- Look at error message, check how far script is running, use breakpoints

What exactly is the problem?

- You can see if variables around breakpoints have values you would expect
- Break down /put parts of the code to test smaller pieces
- Check number of parameters in a function or items in an array

The console helps narrow down the area in which the error is located, so you can try to find the exact error

- You can look at errors, type directly into the console, and write from the script to the console
  - logging data, grouping messages, and other methods

### Breakpoints pause the execution of a script

- You can then check the values stored in variables at that point in time
- You can step through multiple breakpoints one-by-one to see where values change and a problem might occur
- Breakpoints can be conditional
- `debugger;` keyword can be used

If you know that you may get an error, you can handle it gracefully using the `try`, `catch`, `throw`, and `finally` statements.

- Use them to give your users helpful feedback

If you know something might cause a problem for your script, you can generate your own errors before the interpreter creates them using `throw`

[back](../README.md)
