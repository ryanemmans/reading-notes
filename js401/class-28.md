# CLASS 28 NOTES - Component Lifecycle / useEffect() Hook

***1. Why do we not need more .html pages in a multi-page React app?***

- We only need a single `index.html` for the browser to reference because we can use React Router to route to other components (all .js files) from our App.js.
  - This creates multiple pages within a single page application.

***2. If we wanted a component to show up on every page, where would we put it and why?***

- We would put this component inside the `<BrowserRouter/>`, but outside a `<Route/>`. An example of this would be a `Navbar` component.
- In contrast, any component inside a route can be thought of as a specific page.
- Anything that is outside of the BrowserRouter is not declared as an individual route within the application.

***3. What does routing do with the components that were rendered when a new route is requested?***

- Those components become unmounted.
  - Each router creates a *history* object that it uses to keep track of the current location and re-renders the application whenever this location changes.
  - The `<Route/>` renders the appropriate user interface when the current location matches the route’s path.

***4. What does props.children contain?***

- `props.children` is a special prop, automatically passed to every component, that can be used to render the content included between the opening and closing tags when invoking a component.
  - These kinds of components are identified as "boxes".
  - Allows us to compose components, and therefore our front-end interface.

***5. How do useState() and this.setState() differ?***

- `useState()` is a React hook which does not require creating a class.
  - It can be used with functional components, which simplifies the creation of a state component and the function that updates it.
- `this.setState()` is used to handle or change state within a React class component.

***6. Document the following Vocabulary Terms:***

- **State Hook** - lets you add React state to function components, instead of having to convert them to a class.
- **Mounting and Un-Mounting** - DOM creation / "setup" and deletion / "cleanup" in a React component's lifecycle.

- - -

## Preview:

- [Effects Hook](https://reactjs.org/docs/hooks-effect.html)

***1. Which 3 things had you heard about previously and now have better clarity on?***

- React Router
- `useState()` Hook
- `useEffect()` Hook

***2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?***

- Component Lifecycle
- `useEffect()`
- props.children

***3. What are you most excited about trying to implement or see how it works?***

- React Router
- Additional React Hooks
- Switch Component

- - -

Sources:

- [Medium - Intro to React Router](https://medium.com/@ipenywis/intro-to-react-router-for-beginners-multiple-page-apps-461f4729bd3f)
- [freeCodeCamp - React Router Cheatsheet](https://www.freecodecamp.org/news/react-router-cheatsheet/)
- [Medium - Routing in React](https://medium.com/the-andela-way/understanding-the-fundamentals-of-routing-in-react-b29f806b157e)
- [Codeburst.io - props.children](https://codeburst.io/a-complete-guide-to-props-children-in-react-c315fab74e7c)
- [Dev.to](https://dev.to/johnstonlogan/react-hooks-barney-style-1hk7)
- [React Docs - State Hook](https://reactjs.org/docs/hooks-state.html)
- [Learn.co](https://learn.co/lessons/react-component-mounting-and-unmounting)

[back](../README.md)
