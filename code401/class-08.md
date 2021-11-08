# List Comprehensions in Python

List comprehension is a powerful and concise method for creating lists in Python that becomes essential the more you work with lists, and lists of lists.

## Syntax:

```python
new_list=[expression for item in list]
```

we need three things for list comprehension 

1. the expression.
2. the object that the expression will work on.
3. an iterable list of objects to build new_list from.

## Notes about Lists Comprehensions

- List comprehension methods are an elegant way to create and manage lists. 
- In Python, list comprehensions are a more compact way of creating lists. 
- More flexible than for loops, list comprehension is usually faster than other methods.


## Create a List with range()

Example 1: Creating a list with list comprehensions

```python
digits = [x for x in range(10)]

# output
# [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

## Create a List Using Loops and List Comprehension in Python

Example 2: Comparing list creation methods in Python

```python
squares = []

for x in range(10):
    # raise x to the power of 2
    squares.append(x**2)

print(squares)

#output
# [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

## Multiplying Parts of a List

Example 3: Multiplication with list comprehensions

```python
multiples_of_three = [ x*3 for x in range(10) ]

print(multiples_of_three)

# Output

# [0, 3, 6, 9, 12, 15, 18, 21, 24, 27]
```

## Show the first letter of each word using Python

Example 4: Using list comprehensions with strings

```python

# a list of the names of popular authors
authors = ["Ernest Hemingway","Langston Hughes","Frank Herbert","Toni Morrison",
    "Emily Dickson","Stephen King"]

# create an acronym from the first letter of the author's names
letters = [ name[0] for name in authors ]
print(letters)

# output
# ['E', 'L', 'F', 'T', 'E', 'S']
```
