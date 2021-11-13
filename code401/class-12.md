# Pandas in 10

1. in pandas, we import as:

```python
In [1]: import numpy as np

In [2]: import pandas as pd
```

2. Object creation

Creating a Series by passing a list of values, letting pandas create a default integer index:

```python
In [3]: s = pd.Series([1, 3, 5, np.nan, 6, 8])

In [4]: s
Out[4]: 
0    1.0
1    3.0
2    5.0
3    NaN
4    6.0
5    8.0
dtype: float64
```

3. Creating a DataFrame by passing a NumPy array, with a datetime index and labeled columns:

```python

In [5]: dates = pd.date_range("20130101", periods=6)

In [6]: dates
Out[6]: 
DatetimeIndex(['2013-01-01', '2013-01-02', '2013-01-03', '2013-01-04',
               '2013-01-05', '2013-01-06'],
              dtype='datetime64[ns]', freq='D')

In [7]: df = pd.DataFrame(np.random.randn(6, 4), index=dates, columns=list("ABCD"))

In [8]: df
Out[8]: 
                   A         B         C         D
2013-01-01  0.469112 -0.282863 -1.509059 -1.135632
2013-01-02  1.212112 -0.173215  0.119209 -1.044236
2013-01-03 -0.861849 -2.104569 -0.494929  1.071804
2013-01-04  0.721555 -0.706771 -1.039575  0.271860
2013-01-05 -0.424972  0.567020  0.276232 -1.087401
2013-01-06 -0.673690  0.113648 -1.478427  0.524988
```

-------------------

## Getting started tutorials


1. What kind of data does pandas handle? ```DataFrame```

2. How do I read and write tabular data?

```python

In [1]: import pandas as pd
In [2]: file = pd.read_csv("data/file.csv")
In [3]: file
```

3. How do I select a subset of a DataFrame?  ```using the Indexing Operator```

4. How to create plots in pandas?
    - Prepare the data
    - Create the DataFrame
    - Plot the DataFrame using Pandas

    ```python
    df.plot(x ='Unemployment_Rate', y='Stock_Index_Price', kind = 'scatter') 
    ```


