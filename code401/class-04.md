# Classes and Objects

## Classes

Creating a new class creates a new type of object, allowing new instances of that type to be made. Each class instance can have attributes attached to it for maintaining its state. Objects can contain arbitrary amounts and kinds of data. Classes partake of the dynamic nature of Python - they are created at runtime and can be modified further after creation.

- Creating class can be done by:

    ```python
    class MyClass:
        x = 3
    ```

- All classes have a function called ```__init__()```, which is always executed when the class is being initiated.
- Use the ```__init__()``` function to assign values to object properties, or other operations that are necessary to do when the object is being created:

    ```python

    class Person:
        def __init__(self, name, age):
            self.name = name
             self.age = age
    ```

--------

## Objects

A unique instance of a data structure that's defined by its class. An object comprises both data members (class variables and instance variables) and methods

Every object belonging to a class can have different properties. For example, Person(Human) can be treated as a class which has properties such as name, age,gender etc. Each individual will have different values of the properties of class Person. Everyone will also have different names, age and gender.

- To create instances of a class, you call the class using class name and pass in whatever arguments its ```__init__```method accepts.

     ```python

    p1 = Person("John",20)
    print(p1)

    <!-- Output
    John,20
    -->
    
    ```

### The Full code will be as

```python

class Person:
        def __init__(self, name, age):
            self.name = name
             self.age = age

p1 = Person("John",20)

```

- Built-In Class Attributes

Every Python class keeps following built-in attributes and they can be accessed using dot operator like any other attribute −

- ```dict__``` − Dictionary containing the class's namespace.

- ```__doc__```− Class documentation string or none, if undefined.

- ```__name__```− Class name.

- ```__module__```− Module name in which the class is defined. This attribute is ```"__main__"``` in interactive mode.

- ```__bases__``` − A possibly empty tuple containing the base classes, in the order of their occurrence in the base class list.
