# Putting it all together


## React Docs - Thinking in React


1. What is the single responsibility principle and how does it apply to components?

- the Single Responsibility Principle means that a component is required to have only one reason to change. In short, the Single Responsibility Principle means that code with the same functionality should not exist in multiple places.

[source](https://medium.com/@roni.shabo/single-responsibility-in-reactjs-9c60e4163862)


---

2. What does it mean to build a ‘static’ version of your application?

- it means rendering the data model but without any interactivity, so when building a static version we need to typing more than thinking. and when adding interactivity we need to think more than typing. 


[source](https://reactjs.org/docs/thinking-in-react.html)

----

3. Once you have a static application, what do you need to add?

- We need to add components and passing data as props 

----

4. What are the three questions you can ask to determine if something is state?

according of what I know through the class:

-  If its state change, like opening the modal or closing it. we can know that there is a functions behind the scene to handle this.

- in the code, we can know it from the constructor in ```this.state``

- also, if we are doing the state on a modal we will know that the parent pass the state as ```this.state``` to its child, and the child use it as a props. for the functionality. 

-   

5. How can you identify where state needs to live?

For each piece of state in your application:

- Identify every component that renders something based on that state.
- Find a common owner component (a single component above all the components that need the state in the hierarchy).
- Either the common owner or another component higher up in the hierarchy should own the state.
- If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.


---

## Higher-Order Functions


1. What is a “higher-order function”?

Functions that operate on other functions, either by taking them as arguments or by returning them

---

2. Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?

greaterThan function create a new function to check if the value grater than the input one.

line 2 creates a new function that check the current value and the input one. 

```
function greaterThan(n) {
  return m => m > n;
}
let greaterThan10 = greaterThan(10);
console.log(greaterThan10(11));
// → true
```
----

3. Explain how either map or reduce operates, with regards to higher-order functions.

- reduce in higher-order-functions  builds a value by repeatedly taking a single element from the array and combining it with the current value.

-----

## Things I want to know more about