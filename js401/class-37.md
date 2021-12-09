# CLASS 37 NOTES - Redux - Combined Reducers

***1. Why choose Redux instead of the Context API for global state?***

- Redux is used to manage state in a centralized place, which is best for larger apps. The Context API is not built for high-frequency updates and is not a state management tool; however, it does not require any third-party dependencies.

***2. What is the purpose of a reducer?***

- It determines changes to an application’s state. It uses the action it receives to determine this change.

***3. What does an action contain?***

- It contains two keys and their values. The state update is dependent on the value of `action.type`, which is required. `action.payload` is optional and brings a level of structure to how the action object looks.

***4. Why do we need to copy the state in a reducer?***

- Reducers are not allowed to modify existing state. Instead, they must make immutable updates, by copying the existing state and making changes to the copied values. A critical rule of immutable updates is that you must make a copy of every level of nesting that needs to be updated.

***5. Document the following Vocabulary Terms:***

- **immutable state** - its value cannot be changed, so every update creates new value, leaving the old one untouched. If your application state is immutable, you can save all the state's objects in a single store to easily implement undo/redo functionality.
- **time travel in redux** - records of dispatched actions and the state of the Redux store at every point in time, making it possible to inspect state and travel back in time to a previous application state without reloading the page or restarting the app.
- **action creator** -  a function that returns an action object, can dispatch a single action to the store.
- **reducer** - a function that determines changes to an application’s state and uses the action it receives to determine this change.
- **dispatch** - when an action is reported to the store to let it know which things happened.

- - -

## Preview:

- [Multiple Reducers Example](https://www.youtube.com/watch?v=gBER4Or86hE)
- [Redux Docs: Using Combined Reducers](https://redux.js.org/usage/structuring-reducers/using-combinereducers/)
- [Redux Docs: Combined Reducer Syntax](https://redux.js.org/api/combinereducers/)

***1. Which 3 things had you heard about previously and now have better clarity on?***

- Redux
- Actions
- Material UI

***2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?***

- Dispatch
- Immutable state
- Time travel

***3. What are you most excited about trying to implement or see how it works?***

- Material UI
- Gatsby
- Next.js

- - -

Sources:

- [Academind - Redux / Context API](https://academind.com/tutorials/reactjs-redux-vs-context-api)
- [CSS-Tricks - Reducers in Redux](https://css-tricks.com/understanding-how-reducers-are-used-in-redux/)
- [Redux Docs - Reducers](https://redux.js.org/tutorials/fundamentals/part-3-state-actions-reducers)
- [LogRocket - Immutability](https://blog.logrocket.com/immutability-in-react-ebe55253a1cc/)
- [Medium - Time Travel](https://medium.com/the-web-tub/time-travel-in-react-redux-apps-using-the-redux-devtools-5e94eba5e7c0)
- [ReduxBook Action Creators](https://read.reduxbook.com/markdown/part1/04-action-creators.html)

[back](../README.md)
