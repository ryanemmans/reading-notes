# CLASS 9 NOTES - Functional Programming

## ***Concepts of Functional Programming in Javascript***

[https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

- - -

#### **1. What is functional programming?**

- (From [Wikipedia](https://en.wikipedia.org/wiki/Functional_programming))
- Functional programming is a programming paradigm.
- A style of building the structure and elements of computer programs.
- Treats computation as the evaluation of mathematical functions.
- Avoids changing-state and mutable data.

#### **2. What is a pure function and how do we know if something is a pure function?**

- A pure function returns the same result if given the same arguments (or `deterministic`).
- It does not cause any observable side effects.

#### **3. What are the benefits of a pure function?**

- Through pure functions, our programs become easier to understand.
- Pure functions are stable, consistent, and predictable.
- They will always return the same result given the same parameters.
- It is easier to test code, so different contexts can be used.
- Mocking is not needed.

#### **4. What is immutability?**

- Immutability applies to data.
- The state of data cannot be changed after it is created if that data is immutable.
- You would instead create a new object with a new value.

#### **5. What is Referential transparency?**

- **Referential transparency = pure functions + immutable data.**
- A **function** is referentially transparent if it consistently yields the **same** result for the **same** input.

- - -

## ***Node JS Tutorial for Beginners #6 - Modules and require()***

[https://www.youtube.com/watch?v=xHLd36QoS4k&ab_channel=TheNetNinja](https://www.youtube.com/watch?v=xHLd36QoS4k&ab_channel=TheNetNinja)

- - -

#### **1. What is a module?**

- Essentially, a module is just an additional JavaScript file outside of your App.js.
- Modules are created to separate and carry specific functionality in an application.
- They make it much easier for developers to manage, refactor, and extend code.
- They are then called up when their functionality is needed.

#### **2. What does the word ‘require’ do?**

- It is a function on the global object in Node.js.
- It allows us to bring in or source modules in order to utilize their funcitonality.

#### **3. How do we bring another module into the file the we are working in?**

- We use `require` to pass in the path of the module.
- For example, if we have a `count.js`, we would source it and bring it in by typing `require('./count');` at the top of App.js.

#### **4. What do we have to do to make a module available?**

- We have to `export`, or explicitly say which part of the module we want to make available to the files which `require` the module.
- `module.exports = counter;` (in count.js)
- The `export` is what is specifically returned when we `require` a module.
- You would then create a variable that is equal to the `require` in your App.js.
- `let counter = require('./count');`

- - -

## Things I want to know more about

- Where in our applications can we apply functional programming?

[back](../README.md)
