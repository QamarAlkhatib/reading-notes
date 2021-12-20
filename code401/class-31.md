# React2

## React - Conditional Rendering

Conditional rendering in React works the same way conditions work in JavaScript. Use JavaScript operators like if or the conditional operator to create elements representing the current state, and let React update the UI to match them.

## React - Lists & Keys

- Keys help React identify which items have changed, are added, or are removed.

## React - Forms

In HTML, form elements such as ```< input >, <textarea >, and <select >``` typically maintain their own state and update it based on user input. In React, mutable state is typically kept in the state property of components, and only updated with setState().

We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”.

## React - Lifting State

In React, sharing state is accomplished by moving it up to the closest common ancestor of the components that need it. This is called “lifting state up”

## Composition vs Inheritance

Containment: Some components don’t know their children ahead of time. This is especially common for components like Sidebar or Dialog that represent generic “boxes”.
Specialization: Sometimes we think about components as being “special cases” of other components.

Props and composition give you all the flexibility you need to customize a component’s look and behavior in an explicit and safe way.

## Thinking in React

- Step 1: Break The UI Into A Component Hierarchy
![img](https://reactjs.org/static/9381f09e609723a8bb6e4ba1a7713b46/90cbd/thinking-in-react-components.png)

1. FilterableProductTable (orange): contains the entirety of the example
2. SearchBar (blue): receives all user input
3. ProductTable (green): displays and filters the data collection based on user input
4. Whatdisplays a heading for each category
5. ProductRow (red): displays a row for each product

- Step 2: Build A Static Version in React

- Step 3: Identify The Minimal (but complete) Representation Of UI State

- Step 4: Identify Where Your State Should Live

- Step 5: Add Inverse Data Flow
