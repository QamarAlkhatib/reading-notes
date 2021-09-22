# In memory storage

## Understanding the JavaScript Call Stack

1. What is a ‘call’?

    - The call stack is primarily used for function invocation ```(call).```

2. How many ‘calls’ can happen at once?

    - one at a time.

3. What does LIFO mean?

    LIFO: last in first out, the last function that gets pushed into the stack is the first to be pop out, when the function returns.

4. What causes a Stack Overflow?

    - A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error. [resourse](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)

---

## JavaScript error messages

1. What is a ‘refrence error’?

    - when try to use a variable that is not yet declared.

2. What is a ‘syntax error’?

    - this occurs when you have something that cannot be parsed in terms of syntax.

3. What is a ‘range error’?

    - this occurs when give the object invalid length 

4. What is a ‘type error’?

    - this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible

5. What is a breakpoint?

    - A breakpoint is a point in the program where the code will stop executing

6. What does the word ‘debugger’ do in your code?

    - Debuggers allow users to halt the execution of the program, examine the values of variables, step execution of the program line by line, and set breakpoints on lines or specific functions that, when hit, will halt execution of the program at that spot.

## Things I want to know more about