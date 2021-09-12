# State and Props

---------

## React lifecycle

Components can be defined as classes or functions in React. The methods you can use on these are referred to as lifecycle events. These methods are available throughout a component's lifespan and allow you to adjust the UI and application states.

### Questions Answers

1. Based off the diagram, what happens first, the ‘render’ or the ‘componentDidMount’?

- render.
---------

2. What is the very first thing to happen in the lifecycle of React?

- Mounting

------

3. Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates

    1. constructor
    2. render
    3. React Updates
    4. componentDidMount
    5. componentWillUnmount

--------

4. What does componentDidMount do?

- This method is invoked immediately after a component is mounted. If you need to load anything using a network request or initialize the DOM, it should go here

-------

# React Bootstrat Documentation

## Rebuilt with React

As one of the oldest React libraries, React-Bootstrap has evolved and grown alongside React, making it an excellent choice as your UI foundation.

-----

## Bootstrap at its core

Built with compatibility in mind, we embrace our bootstrap core and strive to be compatible with the world's largest UI ecosystem.

--------

## Accessible by default

The React component model gives us more control over form and function of each component.

--------------


# React State Vs Props

Props and state vary in that state is internal and controlled by the component, whereas props are external and controlled by whatever renders the component.

1. What types of things can you pass in the props?

- React allows us to pass values from a parent component down to a child component. The values can be any data type, from strings to functions, objects, etc.


2. What is the big difference between props and state?

- Props and state vary in that state is internal and controlled by the component, whereas props are external and controlled by whatever renders the component.

3. When do we re-render our application?

- When the state or props of a React component change, the component will automatically re-render.

4. What are some examples of things that we could store in state?

- user data
- data from a form

------
## Things I want to know more about

Using the state and props in piece of code.