# Game of Greed 1


## How to use Random Module

The Random module contains some very useful functions.

here are some of them:

- Randint: and we use it of we want random integer:


    ```python
        import random
        print random.randint(0,10)

    ```

- Random we use it if we want a larger number and we can multiple it:

    ```python
    import random
    random.random()* 100
    ```

- choice and its Generate a random value from the sequence sequence.

    ```python
        import random
        myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]
        random.choice(myList)
    ```

- Shuffle The shuffle function, shuffles the elements in list in place, so they are in a random order.

    ```python
        from random import shuffle
    x = [[i] for i in range(10)]
    shuffle(x)

    Output:
    # print x  gives  [[9], [2], [7], [0], [4], [5], [3], [1], [8], [6]]
    # of course your results will vary
    ```

- Randrange: Generate a randomly selected element from range(start, stop, step)

    ```python
        random.randrange(start, stop[, step])

        import random
        for i in range(3):
            print random.randrange(0, 101, 5)

    ```

--------

## What is Risk Analysis

Risk Analysis is a process that helps you to identify and manage potential problems that could undermine key business initiatives or projects. 
Risk is made up of two parts: the probability of something going wrong, and the negative consequences if it does.

## Why use Risk Analysis?

In any software, using risk analysis at the beginning of a project highlights the potential problem areas. After knowing about the risk areas, it helps the developers and managers to mitigate the risks.

## Risk Assessment

In the risk analysis process, these steps prove to be the most important one. It is said that this step is way too complex and should be tackled with the utmost care. After risk identification, assessment has to be dealt programmatically. 

1. Early forecast of unwanted situations in your project.
2. Estimate the potential loss of such situations.
3. Making decision to deal with such situations.
4. Avoid the future consequences.

-------- 

## Test Coverage

Test coverage is defined as a metric in Software Testing that measures the amount of testing performed by a set of test. It will include gathering information about which parts of a program are executed when running the test suite to determine which branches of conditional statements have been taken.

In simple terms, it is a technique to ensure that your tests are testing your code or how much of your code you exercised by running the test.

