# Data Analysis

## What is Jupyter Lab

JupyterLab is a next-generation web-based user interface for Project Jupyter.JupyterLab enables you to work with documents and activities such as Jupyter notebooks, text editors, terminals, and custom components in a flexible, integrated, and extensible manner.

------------ --

## NumPy Tutorial: Data Analysis with Python.

Almost every data analysis or machine learning package for Python leverages NumPy in some way. NumPy was originally developed in the mid 2000s, and arose from an even older package called Numeric.

- steps to work with data using python csv package:

    1. importing the csv library.
    2. open the csv file
    3. with the file open, create a new csv.reader object.
    4. pass the keyword ```delimiter=";"``` to make sure that the records are split up on the semicolon character instead of the default comma character.
    carr the list type to get all the rows from the file.
    5. assign the result to what we want. then printing the rows number that we want

    here is an example:

    ```python
    import csv
    with open('name of the file.csv','r') as file
        name = list(csv.reader(file,delimiter=';'))
    print(name[:3])
    ```

    we can calculate or edit the data once the data has been printed out.

------ 

## Numpy 2-Dimensional Arrays

Notes:

> A 2-dimensional array is also known as a matrix

> In a NumPy array, the number of dimensions is called the rank, and each dimension is called an axis. So the rows are the first axis, and the columns are the second axis.

> One of the limitations of NumPy is that all the elements in an array have to be of the same type,

> if we include the header row, all the elements in the array will be read in as strings

### Creating A NumPy Array

If we pass in a list of lists, it will automatically create a NumPy array with the same number of rows and columns. Because we want all of the elements in the array to be float elements for easy computation, we can use the numpy.array function to compute an element-by-element array.

using numpy with the previous code:

```python
import csv
with open('name of the file.csv','r') as file
        name = list(csv.reader(file,delimiter=';'))
import numpy as np
name = np.array(name[1:], dtype=np.float)
```

We can check the number of rows and columns in our data using the shape property of NumPy arrays:

```python 
name.shape
```

- The topic is very huge to cover, here is the [resource](https://www.dataquest.io/blog/numpy-tutorial-python/)