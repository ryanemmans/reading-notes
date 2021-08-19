# CLASS 4 NOTES - React and Forms

## ***Forms***

[https://reactjs.org/docs/forms.html](https://reactjs.org/docs/forms.html)

- - -

#### ***1. What is a ‘Controlled Component’?***

- A controlled component is an input form element whose value is controlled by React and at the same time controls what happens when a user provides input.
- It handles user submission and has access to the entered data.

#### ***2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.***

- We should update the state as the user enters their responses to make the form more responsive.
- This gives React more control over form input.
- Therefore having the input's value be driven by the state.
- This value can then be passed to other UI elements.

#### ***3. How do we target what the user is entering if we have an event handler on an input field?***

- To target specific user input, we can add a name attribute to each element
- The handler function can then decide what happens based on the value of `event.target.name`.

- - -

## ***JavaScript — The Conditional (Ternary) Operator Explained***

[https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff](https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff)

#### ***1. Why would we use a ternary operator?***

- It enables major refactoring of code.
- We can take a conditional `if` statement and turn it into one line to yield the same results.

#### ***2. Rewrite the following statement using a ternary statement:***

```js
  if(x===y){
 console.log(true);
  } else {
 console.log(false);
  }
```

```js
  x===y ? true : false;
```

- - -

## Things I want to know more about

- A better understanding of controlled components and how they affect forms and state.
- More familiarity and applied practice using ternary operators, especially with multiple conditions and operations.

[back](../README.md)
