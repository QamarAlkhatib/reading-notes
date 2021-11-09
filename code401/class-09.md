# Game of Greed 4

## ***Dunder Methods***

### What Are Dunder Methods?

In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example ```__init__``` or ```__str__```.

Dunder methods let you emulate the behavior of built-in types

as an example to use ```len``` with class:

```python
class LenSupport:
    def __len__(self):
        return 42

>>> obj = LenSupport()
>>> len(obj)
42

```

---

#### Here are an example of using Dunder Methods

- Object Initialization: ```__init__```

    The constructor takes care of setting up the object

    ```python

    def __init__(self, ):
            """
            This is the constructor that lets us create
            objects from this class
            """
        
    ```

- Object Representation: ```__str__```, ```__repr__```

    1. ```__str___```: string representation of an object
    2. ```__repr__```: object representation of an object

    ```python
    
    class string_test(): 
        def __repr__(self):
            pass
            
        def __str__(self):
            pass
            
    string = 'Hi'
    print(str(string))
    print(repr(string))
    # output
    # Hi
    #'Hi' 
    
    ```
- Iteration: ```__len__, __getitem__, __reversed__```

- Operator Overloading for Comparing: ```__eq__, __lt__```

------------

## ***What is probability?***

At the most basic level, probability seeks to answer the question, “What is the chance of an event happening?” An event is some outcome of interest. To calculate the chance of an event happening, we also need to consider all the other events that can occur. The quintessential representation of probability is the humble coin toss. In a coin toss the only events that can happen are:

- Flipping a heads
- Flipping a tails

## ***The data and the distribution***

distribution:  In probability, the normal distribution is a particular distribution of the probability across all of the events. The x-axis takes on the values of events we want to know the probability of. The y-axis is the probability associated with each event, from 0 to 1. 