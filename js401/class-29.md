# CLASS 29 NOTES - Advanced State with Reducers

***1. How can we ensure that an effect hook runs only once?***

- To run an effect only once on mount and unmount, you can pass an empty array ([]) as a second argument. This tells React that your effect doesn’t depend on any values from props or state, so it never needs to re-run.

***2. Can useState() update more than one state variable at the same time?***

- I don't believe so. You would need to use two different useState calls which would update state variables separately.

***3. Is useState() synchronous?***

- In React, all state updates are asynchronous, both in classed based components as well as with functions and hooks.

***4. Document the following Vocabulary Terms:***

- **State Hook** - lets you add React state to function components, instead of having to convert them to a class.
- **Component Lifecycle** - Phases or methods of a component that are used for mounting, updating, unmounting, and error handling.

- - -

## Preview:

- [useReducer Hook](https://reactjs.org/docs/hooks-reference.html#usereducer)
- [Ultimate Guide to useReducer](https://blog.logrocket.com/guide-to-react-usereducer-hook/)

***1. Which 3 things had you heard about previously and now have better clarity on?***

- `useState()`
- `useEffect()`
- Component Lifecycle

***2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?***

- `useReducer()`
- `useContext()`
- GitHub pages for React apps.

***3. What are you most excited about trying to implement or see how it works?***

- `useReducer()`
- `useContext()`
- UI libraries

- - -

Sources:

- [React useEffect](https://reactjs.org/docs/hooks-effect.html)
- [Egghead.io](https://egghead.io/lessons/react-handle-multiple-state-values-when-using-usestate-react-hook)
- [dev.to](https://dev.to/bytebodger/synchronous-state-with-react-hooks-1k4f)
- [React.Component](https://reactjs.org/docs/react-component.html)

[back](../README.md)
