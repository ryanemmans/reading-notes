# CLASS 5 NOTES - Putting It All Together

## ***Thinking in React***

[https://reactjs.org/docs/thinking-in-react.html](https://reactjs.org/docs/thinking-in-react.html)

- - -

#### ***1. How would you break a mock into a component heirarchy?***

- Firstly, draw a box around each component and subcomponent and give them all names.
- You will need to determine which components will be on their own.
- If a component will be doing multiple things, it should be decomposed into smaller components.
- By separating your UI into components, each one should match one piece of your data model.
- Once components are identified, they can be arranged into a hierarchy.

#### ***2. What is the `single responsibility principle` and how does it apply to components?***

- It states that "every module, class, or function ... should have responsibility over a single part of a program's functionality." - (Source: [Wikipedia](https://en.wikipedia.org/wiki/Single-responsibility_principle))
- It applies to components by suggesting that they should ideally only be doing one thing.

#### ***3. What does it mean to build a ‘static’ version of your application?***

- A static version is essentially taking your data model and rendering a UI that lacks interactivity.
- At this time you will begin building your components and use props.
- You can typicaly build top-down (for simple examples) or bottom-up (for larger projects).

#### ***4. Once you have a static application, what do you need to add?***

- You will need to then make your UI interactice by triggering  your data model.
- This will be achieved with state.

#### ***5. What are the three questions you can ask to determine if something is state?***

1. Is it passed in from a parent via props?
2. Does it remain unchanged over time?
3. Can you compute it based on any other state or props in your component?

- If the answer to any of these is yes, it will not be state.

#### ***6. How can you identify where state needs to live?***

- Identify which components will render based on state.
- Find a common owner component.
- Determine if the common owner or another component higher up should own the state.
- If a component cannot be found, create a new component solely for holding state.
  - Add it to the heirarchy above common owner component.

- - -

## Things I want to know more about

- What is Babel and how does it apply to JavaScript?
- How can we determine our hierarchy with larger, more complex programs?
- The structure of where to pass props and where state should live still confuses me.

[back](../README.md)
