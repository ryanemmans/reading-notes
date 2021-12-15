# CLASS 41 NOTES - React Native

***1. Compare and Contrast Redux Toolkit with Redux “Ducks”***

- Redux includes several utility functions, including store setup, defining reducers, immutable update logic, and creating "slices" of state without writing any action creators or action types by hand. It also includes Redux addons like Thunk and Reselect for async logic and writing selector functions.
- Ducks bundles reducers, action types, and actions all into isolated Redux modules.

***2. What is the principle advantage of Redux Toolkit***

- Toolkit is an opinionated, "batteries-included" toolset that makes Redux development efficient. It easily addresses store configuration, minimizes packages, and removes a lot of the boilerplate code needed by Redux.

***3. Document the following Vocabulary Terms:***

- **Redux Toolkit Slices** - a "slice" of the redux store. They accept an initial state, an object full of reducer functions and a slice name. They automatically generate action creators and action types that correspond to the reducers and state and use createAction and createReducer internally.
- **Namespace** - allows multiple instances of components to co-exist with independent state when used on actions, reducers, and state.

- - -

## Preview:

- [Getting Started with React Native](https://reactnative.dev/docs/getting-started)
- [React Native Basics](https://reactnative.dev/docs/tutorial)
- [React Native](https://reactnative.dev/)
- [Expo](https://expo.dev/)
- [Expo Snack](https://snack.expo.dev/)
- [Ejecting](https://docs.expo.dev/expokit/eject/?redirected)

***1. Which 3 things had you heard about previously and now have better clarity on?***

- Redux toolkit
- Slices
- React Native

***2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?***

- Ducks
- React Native
- Expo

***3. What are you most excited about trying to implement or see how it works?***

- Redux Toolkit
- React Native
- TypeScript

- - -

Sources:

- [Redux Overview](https://redux.js.org/redux-toolkit/overview)
- [Medium - createSlice](https://medium.com/geekculture/understanding-createslice-in-redux-toolkit-reactjs-eca8d20f45d7)
- [Redux Namespaces](https://github.com/9technology/redux-namespaces)

[back](../README.md)
