# CLASS 10 NOTES - In Memory Storage

## ***The JavaScript Call Stack - What It Is and Why It's Necessary***

[https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)

*- Code examples taken from text.*

- - -

#### **1. What is a ‘call’?**

- A call is synchronous.
- It is used primarily for function invocation.
- The call stack is single, therefore function execution takes place one at a time.

#### **2. How many ‘calls’ can happen at once?**

- Only one call can happen at a time.

#### **3. What does LIFO mean?**

- LIFO stands for "Last In, First Out."
- This means that the last function to be *pushed* into the stack will be the first to *pop* out when the function returns.

#### **4. Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.**

- (Taken from article)

```js
function firstFunction(){
  throw new Error('Stack Trace Error');
}

function secondFunction(){
  firstFunction();
}

function thirdFunction(){
  secondFunction();
}

thirdFunction();
```

- `firstFunction()` is the last function to go into the stack.
- The error is thrown when `firstFunction()` is popped out.

![Call Stack](https://cdn-media-1.freecodecamp.org/images/QgR2uIk7tW0YNz0Xm8g0jAPeRFI0e4sCejsv)


#### **5. What causes a Stack Overflow?**

- A stack overflow occurs when there is a function that calls itself (recursive) without an exit point.
- There is a maximum call stack that the browser can accomodate before throwing a stack error.

- - -

## ***JavaScript error messages && debugging***

[https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c)

*- Code examples taken from text.*

- - -

#### **1. What is a ‘refrence error’?**

- A reference error happens when a variable is attempted to be used, but it has not yet been declared.

```js
foo = 'Hello' // Uncaught ReferenceError: foo is not defined
let foo
```

#### **2. What is a ‘syntax error’?**

- A syntax error is when you have something that cannot be parsed in terms of syntax.

```js
JSON.parse( {'foo': 'bar'} ) // Uncaught SyntaxError: Unexpected token o in JSON at position 1
```

This example would need to be changed to:

```js
JSON.parse('{"foo":"bar"}')
```

#### **3. What is a ‘range error’?**

- A range error will occur if you try to manipulate an object by giving it an invalid length

```js
var foo= []
foo.length = foo.length -1 // Uncaught RangeError: Invalid array length
```

#### **4. What is a ‘type error’?**

- A type error shows up when the types you are trying to use or access (string, number, etc.) are incompatible.
- One of the most frequent errors in JavaScript.

```js
var foo = {}
foo.bar // undefined
foo.bar.baz // Uncaught TypeError: Cannot read property 'baz' of undefined
```

#### **5. What is a breakpoint?**

- A break point is used for debugging.
- It will make your program stop at a certain point only if a condition has been met.

#### **6. What does the word ‘debugger’ do in your code?**

- A *debugger* statement can be put in a line of code that you want to break.
- You can run the debugger by pressing F5 in VSCode.

- - -

## Things I want to know more about

- A clearer understanding of how call stacks work.
- More practice with using the debugger tool.
- A better understanding of breakpoints.
- How to understand specific errors and use them to my advantage as they apply to fixing bugs.

[back](../README.md)
