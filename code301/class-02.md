# CLASS 2 NOTES - State and Props

## ***React: Component Lifecycle Events***

[https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093](https://medium.com/@joshuablankenshipnola/react-component-lifecycle-events-cb77e670a093)

- - -

#### ***1. Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?***

- It appears that render, which takes place in the Render phase, happens before 'componentDidMount', which takes place in the Commit phase.

#### ***2. What is the very first thing to happen in the lifecycle of React?***

- The Mounting phase is at the beginning of the life cycle, and the constructor for a React component is called before it is mounted.

#### ***3. Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates*** 

- constructor
- render
- React updates
- componentDidMount
- componentWillUnmount

#### ***4. What does componentDidMount do?***

- It is a method that is immediately invoked after a component is mounted. It can be used to connect to APIs to receive content once components are rendered.



- - -

## ***React State Vs Props***

[https://www.youtube.com/watch?v=IYvD9oBCuJI&ab_channel=WebDevSimplified](https://www.youtube.com/watch?v=IYvD9oBCuJI&ab_channel=WebDevSimplified)

#### ***1. What types of things can you pass in the props?***

- Props are similar to passing arguments to a function.
- When you want to render a React component, you will pass the props of that component.
- Props are what you want to initialize your component to do or how you want it to render.
- For example: We would pass the initial count of a counter component which would be at 0, or a title and subtitle in a component.

#### ***2. What is the big difference between props and state?***

- The big difference between props and state is with props you would pass into a component, whereas state is handled inside of a component and it can be updated.
- Alternately props are handled outside of a component. For example with the counter application, the current, up-to-date count would be handled inside the state.

#### ***3. When do we re-render our application?***

- A section of our application will be re-rendered when we change the state inside of a component to affect that specific section.
- If a component does not need to be re-rendered, it does not need any state.

#### ***4. What are some examples of things that we could store in state?***

- Anything that would need to be re-rendered as a result of something the user has done would require state, such as any changes that would need to be updated to an application.
- A good example of when to use state would be the count of a counter application which would change and re-render or a form that would be filled out by the user.

- - -

## Things I want to know more about

- More visual examples of how props and state apply to parent and sub classes.
- A better understanding of component lifecycle events.
- How mounting and unmounting actually works.

[back](../README.md)
