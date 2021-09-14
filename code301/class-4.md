# React and Forms


1. What is a ‘Controlled Component’?

- A controlled component is a component that renders form elements and controls them by keeping the form data in the component's state.

----

2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.

- both of them will work,  in the second way: when React is responsible for maintaining and setting its state. The state is kept in sync with the input’s value, meaning that changing the input will update the state, and updating the state will change the input.

----

3. How do we target what the user is entering if we have an event handler on an input field?

after adding the setState on the ChangeInput function, we can target the event as ``` event.target.value ``` 

-----

## The Conditional (Ternary) Operator Explained

1. Why would we use a ternary operator?

- A ternary operator allows you to assign one value to the variable if the condition is true, and another value if the condition is false. A ternary operator makes the assignment of a value to a variable easier to see, because it's contained on a single line instead of an if else block.

2. Rewrite the following statement using a ternary statement:

```
  if(x===y){
    console.log(true);
  }else {
    console.log(false);
  }
```

Using ternary statment: 

``` x===y ? true : false; ```
