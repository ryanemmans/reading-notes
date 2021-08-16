# CLASS 1 NOTES - Introduction to React and Components

## ***Component-Based Architecture***

https://www.tutorialspoint.com/software_architecture_design/component_based_architecture.htm

- - -

Component-based architecture breaks down a design into functional or logical components.

- Communication interfaces that contain methods, events, and properties
- Divides problem into sub-problems

Primary objective is to ensure **component reusability**

Advantages over object oriented approaches

- Reduced time and development cost
- Increased reliability through reuse

### ***1. What is a Component?***

- A modular, portable, replaceable, and reusable set of well-defined functionality
- A software object, interacting with other components, with certain functionality
- A unit of composition with specified interface and explicit context dependencies
  - Can be deployed independently
  - Subject to composition by third parties

### ***2. What are the Characteristics of a Component?***

- **Reusability** - usually designed to be reused in different situations
- **Replaceable** - may be freely substituted with other similar components
- **Not context specific** - designed to operate in different environements
- **Extensible** - extended from existing components to provide new behavior
- **Encapsulated** - allow caller to use functionality
- **Independent** - Minimal dependencies on other components

### ***3. What are the advantages of using component based architecture?***


- **Ease of deployment** - easier to replace existing versions
- **Reduced cost** - through third party components
- **Ease of development** - doesn't impact other parts of the system
- **Reusable** - across several applications of systems
- **Modification of technical Complexity** - component container and its services
- **Reliability** - each component enhances system via reuse
- **System maintenance and evolution** - easy to change and update
- **Independent** - flexible connectivity of components

### Views of a Component

- Object-oriented view
  - Set of one or more cooperating classes
  - Defining of interfaces that enable classes to communicate
- Conventional view
  - Functional element or module of a program
- Process-related view
  - System builds from existing components in a library

### Principles of Component-based Design

- Software system is made up of reusable component units
- Each component has its own interfaces and hides implementations
- Should be extended without the need for modifications
- Do not depend on other components
- Component interaction is specified by interfaces
- Can extend to other components and still offer its own extension points
  - Plug-in based architecture

### Component-Level Design Guidelines

- Specified meaningful naming conventions
- Entities can exist independently
- Recognizes entities as new components
- Dependencies from left to right and top to bottom (base class to derived classes)

### Conducting Component Level Design

- Design classes must correspond to infrastructure domain
- Unacquired classes are reusable components
- Appropriate interfaces for each component, with attributes data types and structures
- Persistent data sources
- Behavioral representations
- Deployment diagrams

- - -

## ***What Is “Props” and How To Use It In React?***

https://itnext.io/what-is-props-and-how-to-use-it-in-react-da307f500da0

- *Code examples referenced from the text*

- - -

### ***1. What is props short for?***

- A special keyword in React, which simply stands for **"properties"**.

### ***2. How are props used in React?***

- Props are used to pass data from one component to another, similar to function arguments

### ***3. What is the flow of props?***

- Data with props is passed in a **uni-directional flow**.
  - One way from parent to child
- Props data is read-only (or immutable)
  - Data from parent should not be changed by child components

### Using Props in React

1. An attribute needs to be defined with its value (data)
2. Then passed to child component(s) by using Props
3. We must then render the Props Data

Interpolation `{}` will be used to define attributes and assign values.

```jsx
<ChildComponent text={“I’m the 1st child”} />
```

Next, we will pass props into the component to bring all necessary data, similar to arguments in a function

```jsx
const ChildComponent = (props) => {  
  return <p>I'm the 1st child!</p>; 
};
```

Then we run a `console.log(props);` to see that we have an object

We will finally render the data using string interpolation.

```jsx
class ParentComponent extends Component {  
  render() {
    return (
      <h1>
        I'm the parent component.
        <ChildComponent text={"I'm the 1st child"} />
        <ChildComponent text={"I'm the 2nd child"} />
        <ChildComponent text={"I'm the 3rd child"} />
      </h1>
    );
  }
}
```

Individual prop data will now render, converting the components from static to dynamic.

- - -

## Things I Want To Know More About

- How do we seperate parent and child react files?
- How can we practice creating components?
- How are components connected to the interface?
- Is JSX completely separate from JavaScript?

[back](../README.md)
