# CLASS 3 NOTES - Passing Functions as Props

## ***Lists and Keys***

[https://reactjs.org/docs/lists-and-keys.html](https://reactjs.org/docs/lists-and-keys.html)

- - -

#### ***1. What does .map() return?***

- `.map()` will return a new array of elements from a provided array.

#### ***2. If I want to loop through an array and display each value in JSX, how do I do that in React?***

- With React and JSX, we can put an array element inside curly braces `{}` inside our tag element such as `<li>`.

#### ***3. Each list item needs a unique ____.***

- **KEY**
- A key is special string attribute needed when creating lists.

#### ***4. What is the purpose of a key?***

- A key will help React identify changes in items, when items are added or removed.
- They also give a stable identity to the items inside an array.

- - -

## ***How to Use the Spread Operator (...) in JavaScript***

[https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab)

#### ***1. What is the spread operator?***

- It is a syntax referring to an ellipses (`...`) to expand an iterable object into a list of arguments

#### ***2. List 4 things that the spread operator can do.***

- Add items to arrays
- Combine arrays or objects
- Spread an array out into a function's arguments.
- Use Math functions


#### ***3. Give an example of using the spread operator to combine two arrays.***

- Also known as array concatenation:

```js
const a = [1,2,3]
const b = [4,5,6]
const c = [...a,...b]
console.log(...c) // 1 2 3 4 5 6
```

#### ***4. Give an example of using the spread operator to add a new item to an array.***

```js
const a = [1,2,3]
const b = [...a];
console.log(b) // Array(3) [1,2,3]

a[0] = 6
console.log(...[...a,'...',...b]) 6 2 3 ... 1 2 3
```

#### ***5. Give an example of using the spread operator to combine two objects into one.***

```js
const objOne = {a}
const objTwo = {b}
const objThree = {...objOne, ...objTwo, c}
console.log(objectThree) // Object { a, b, c }
```

- - -

## ***React - How to Pass Functions between Components - Episode 22***

[https://www.youtube.com/watch?v=c05OL7XbwXU&ab_channel=SteveGriffith-Prof3ssorSt3v3](https://www.youtube.com/watch?v=c05OL7XbwXU&ab_channel=SteveGriffith-Prof3ssorSt3v3)

#### ***1. In the video, what is the first step that the developer does to pass functions between components?***

- The first thing he did was create an `increment` function below his constructor. This was where the state that he wanted to change lived.

#### ***2. In your own words, what does the increment function do?***

- The `increment` function passes in an object from the constructor function, loops through the array of objects, and modifies the array by incrementing a specific object count with state.
- By using the `.map()` method, a new array is created.

#### ***3. How can you pass a method from a parent component into a child component?***

- To pass a method from a parent component into a child component, you would use `this.props.methodName()`.

#### ***4. How does the child component invoke a method that was passed to it from a parent component?***

- By using `this.props.methodName()`, you must pass in the object property that you want to send back up to the method to change the state, again by using `this.props`.

```js
this.props.methodName(this.props.object)
```

- This will then pass down the new count value.

- - -

## Things I want to know more about

- I'd like to become more familiar with incorporating keys.
- Spread seems very cool and useful, I would like to get practice applying it.
- A better understanding of using `.map()` in conjunction with changing the state of array objects.

[back](../README.md)
