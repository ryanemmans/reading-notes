# CLASS 32 NOTES - Context API - Behaviors

***1. When you have multiple contexts, what component type should you use (class/function) and why?***

- A class component would provide the initial context values. You would then use a functional component to consume the multiple contexts. This enables context to re-render fast.

***2. What are some good use cases for using the Context API for global state?***

- When this global state changes, it triggers a re-render of all of the children components which produces new data to show up in the UI. WHen state is global, context eliminates the need to pass props between components.

***3. How can you best test context?***

- The best way to test context is to make our tests unaware of its existence and avoid mocks. We want to use behavioral testing and mimic the way they would run in our applications through integration testing.

***4. Document the following Vocabulary Terms:***

- **context** - Provides a way to pass data through the component tree without having to pass props down manually at every level.
- **useContext()** - Accepts a context object and returns the current context value for that context. The current context value is determined by the value prop of the nearest provider above the calling component in the tree.
- **static context** - eqivalent to `useContext(MyContext)` in a class, or `<MyContext.Consumer>`

- - -

## Preview:

- [Context API](https://reactjs.org/docs/context.html)
- [Hooks and Context Example](https://medium.com/swlh/snackbars-in-react-an-exercise-in-hooks-and-context-299b43fd2a2b)
- [React Context Links](https://github.com/diegohaz/awesome-react-context)

***1. Which 3 things had you heard about previously and now have better clarity on?***

- Context
- Global state
- Providers and consumers

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

- [Breathe Co](https://content.breatheco.de/en/lesson/context-api)
- [samdawson.dev](https://www.samdawson.dev/article/react-context-testing)

[back](../README.md)
