# CLASS 33 NOTES - `<Login />` and `<Auth />`

***1. Why is the Context API useful?***

- The Context API is useful for sharing data that can be considered global. Any situation where you have to pass a prop through a component so it reaches another component somewhere down the tree is where you can use the Context API.

***2. Can a component outside of a provider get its context?***

- Yes it can. To access a React context outside of a provider, we can use the `useContext` hook.

***3. What are some common use cases for using the Context API?***

- Examples for using the Context API would be a currently authenticated user, theme settings, or preferred language for the application.

***4. Describe “Context Hell”***

- It is the result of taking advantage of the React Context API which leads to many Providers nested inside each other as children.

***5. Document the following Vocabulary Terms:***

- **global state** - The data that is shared between all the components within a React application
- **global context** - Designed to share data that can be considered “global” for a tree of React components.
- **provider** - Allows consuming components to subscribe to context changes. Accepts a value prop to be passed to consuming components that are descendants of this Provider.
- **consumer** - A React component that subscribes to context changes. Using this component lets you subscribe to a context within a function component.

- - -

## Preview:

- [What is role based access control?](https://digitalguardian.com/blog/what-role-based-access-control-rbac-examples-benefits-and-more)
- [React-cookies component](https://www.npmjs.com/package/react-cookies)
- [React-cookie library](https://www.npmjs.com/package/react-cookie)

***1. Which 3 things had you heard about previously and now have better clarity on?***

- React Context API
- Global state
- Providers and consumers

***2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?***

- Redux
- RBAC in React
- react-cookies

***3. What are you most excited about trying to implement or see how it works?***

- Redux
- BlueprintJS
- Custom hooks

- - -

Sources:

- [Pusher](https://blog.pusher.com/react-context-api/)
- [thewebdev.info](https://thewebdev.info/2021/05/28/how-to-access-a-react-context-outside-of-the-render-function/)
- [dev.to](https://dev.to/alfredosalzillo/the-react-context-hell-7p4)
- [EnderTech](https://endertech.com/blog/using-reacts-context-api-for-global-state-management#:~:text=To%20put%20it%20simply%2C%20global,the%20components%20re%2Drender%20accordingly.)
- [React Context](https://reactjs.org/docs/context.html#:~:text=Context%20is%20designed%20to%20share,class%20App%20extends%20React.)

[back](../README.md)
