# CLASS 31 NOTES - Context API

***1. Describe use cases useState() vs useReducer()***

- useReducer is usually preferable to useState when you have complex state logic that involves multiple sub-values or when the next state depends on the previous one.
- useReducer also lets you optimize performance for components that trigger deep updates because you can pass dispatch down instead of callbacks.

***2. Why do custom hooks need the use prefix?***

- The "use" prefix is an important convention which helps us to check for violations of rules of Hooks and tells us if a certain function contains calls to Hooks inside of it.

***3. What do custom hooks usually do?***

- They let you extract component logic into reusable functions. They are JavaScript functions that may call other Hooks.

***4. Using any list of custom hooks, research and name one that you think will be useful in your applications***

- `useRouter()`
- `useAuth()`
- `useAsync()`
- `useEventListener()`
- `useDarkMode()`
- etc.

***5. Describe how a hook that fetches API data might work***

- Data can be fetched with `useEffect` and `useState`.
- We would add the API call to a `fetchData` function using Axios.
- Call `fetchData` in `useEffect`.
- Add the response data within JSX to display the API data.
- Use the `useCallback` hook to prevent an infinite loop caused by `useEffect`.

***6. Document the following Vocabulary Terms:***

- **reducer** - a function that determines changes to an application's state. It uses the action it receives to determine this change.

- - -

## Preview:

- [Context API](https://reactjs.org/docs/context.html)
- [Hooks and Context Example](https://medium.com/swlh/snackbars-in-react-an-exercise-in-hooks-and-context-299b43fd2a2b)
- [React Context Links](https://github.com/diegohaz/awesome-react-context)

***1. Which 3 things had you heard about previously and now have better clarity on?***

- `useReducer`
- Custom hooks
- Context

***2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?***

- Context
- BlueprintJS
- Custom hooks

***3. What are you most excited about trying to implement or see how it works?***

- Context
- Redux
- BlueprintJS

- - -

Sources:

- [React Hooks API Reference](https://reactjs.org/docs/hooks-reference.html)
- [Building Your Own Hooks](https://reactjs.org/docs/hooks-custom.html)
- [BetterProgramming](https://betterprogramming.pub/quick-intro-to-react-hooks-6e8a44ae4aa6)
- [Usehooks.com](https://usehooks.com/)
- [RapidAPI Last Call](https://rapidapi.com/blog/react-hooks-fetch-data-api/)
- [CSS Tricks](https://css-tricks.com/understanding-how-reducers-are-used-in-redux/#:~:text=A%20reducer%20is%20a%20function,so%20that%20they%20behave%20consistently.)

[back](../README.md)
