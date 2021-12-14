# CLASS 39 NOTES - Redux - Additional Topics

***1. What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application?***

- In Redux, you would use `createStore` which takes preloaded state as its second argument. You could also use the `useEffect` hook to load state from the store.

***2. When using a thunk/async action that dispatches the actual action, which do you export from your reducer?***

- You would export the function

***3. Document the following Vocabulary Terms:***

- **Middleware** - in Redux, it provides a third-party extension point between dispatching an action, and the moment it reaches the reducer. Used for logging, crash reporting, talking to an async API, routing, and more.
- **Thunk** - a pattern of writing functions with logic inside that can interact with a Redux store's `dispatch` and `getState` methods.

- - -

## Preview:

- [Redux Toolkit (RTK)](https://redux-toolkit.js.org/)
- [RTK Tutorial](https://redux-toolkit.js.org/tutorials/overview)
- [mobX](https://mobx.js.org/getting-started.html)
- [HookState](https://hookstate.js.org/)

***1. Which 3 things had you heard about previously and now have better clarity on?***

- Redux store
- Thunk
- Redux middleware

***2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?***

- Redux Toolkit
- React Native
- Jamstack

***3. What are you most excited about trying to implement or see how it works?***

- Redux Tooklit
- Jamstack
- Stackbit

- - -

Sources:

- [Redux Async Logic](https://redux.js.org/tutorials/essentials/part-5-async-logic#using-middleware-to-enable-async-logic)
- [Redux Thunk](https://redux.js.org/usage/writing-logic-thunks#thunk-overview)
- [Redux Middleware](https://redux.js.org/understanding/history-and-design/middleware#understanding-middleware)

[back](../README.md)
