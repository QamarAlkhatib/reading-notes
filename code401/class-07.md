# Game of Greed 2

## Modules: The Global Scope

Internally, Python turns your program’s main script into a module called ```__main__``` to hold the main program’s execution. In Python, the notions of global scope and global names are tightly associated with module files.

- to check if you are in the main module you can check by typing:

    ```python
    >>> __name__
    '__main__'

    ```

Python's 'main' module or script is the entry point to your program. It contains the code that executes when you run a Python program or interactive session. From this point on, you can say that your main global scope is the scope of ```__main__```.

To inspect the names within your main global scope, you can use dir(). If you call dir() without arguments, then you’ll get the list of names that live in your current global scope. Take a look at this code:

```python
>>> dir()
['__annotations__', '__builtins__', '__doc__', '__loader__', '__name__', '__package__', '__spec__']

```

There's only one global Python scope per program execution. This scope remains in existence until the program terminates and all its names are forgotten. Otherwise, the next time you were to run the program, the names would remember their values from the previous run of the program.

- Whenever you assign a value to a name in Python, one of two things can happen:

    1. You create a new name
    2. You update an existing name

If you try to assign a value to a global name inside a function, you'll be creating that name in the function's local scope. This means you won't be able to change most variables that have been defined outside the function from within the function itself.

Here is an example:

```python
    
    >>> var = 100  # A global variable
    >>> def increment():
    ...     var = var + 1  # Try to update a global variable
    ...
    >>> increment()
    Traceback (most recent call last):
    File "<stdin>", line 1, in <module>
        increment()
    File "<stdin>", line 2, in increment
        var = var + 1
    UnboundLocalError: local variable 'var' referenced before assignment

```

Modifying global names is generally considered bad programming practice because it can lead to code that is:

- Difficult to debug: Almost any statement in the program can change the value of a global name.

- Hard to understand: You need to be aware of all the statements that access and modify global names.

- Impossible to reuse: The code is dependent on global names that are specific to a concrete program.

Good programming practice recommends using local names rather than global names. Here are some tips:

- Write self-contained functions that rely on local names rather than global ones.
- Try to use unique objects names, no matter what scope you’re in.
- Avoid global name modifications throughout your programs.
- Avoid cross-module name modifications.
- Use global names as constants that don’t change during your program’s execution.

----

## The global Statement

With a global statement, you can define a list of names that are going to be treated as global names. All the names in this list will be mapped to the global or module scope in which you define them. You can also use multiple global statements with a name and multiple names separated by commas. Here is an example:

```python
>>> counter = 0  # A global name
>>> def update_counter():
...     global counter  # Declare counter as global
...     counter = counter + 1  # Successfully update the counter
...
>>> update_counter()
>>> counter
1
>>> update_counter()
>>> counter
2
>>> update_counter()
>>> counter
3
```

-----

## globals()

In Python, globals() is a built-in function that returns a reference to the current global scope or namespace dictionary. This dictionary always stores the names of the current module. This means that if you call globals(name) in a given module, then you'll get a dictionary containing all the names that you've defined in that module.

```python
>>> globals()
{'__name__': '__main__',..., '__builtins__': <module 'builtins' (built-in)>}
>>> my_var = 100
>>> globals()
{'__name__': '__main__',..., 'my_var': 100}

```

-----

## locals()

This function updates and returns a dictionary that holds a copy of the current state of the local Python scope or namespace. When you call locals() in a function block, you get all the names assigned in the local or function scope up to that point.
    - Here is an example:
    
```python
>>> def func(arg):
...     var = 100
...     print(locals())
...     another = 200
...
>>> func(300)
{'var': 100, 'arg': 300}

```

Whenever you call locals() inside a function, the resulting dictionary contains the name var mapped to the value 100 and arg mapped to 300. Since locals() only grabs the names assigned before you call it, another is not in the dictionary. If you're calling locals() in the global scope, then you'll get the same dictionary that you would get if you were to call globals() inside func().

```python
>>> locals()
{'__name__': '__main__',..., '__builtins__': <module 'builtins' (built-in)>}
>>> locals() is globals()
True
```
