
## based on what I've learned for Javascript Operators and Loops

## **Operators**

In JS we have 10 types of Operators, and I will discuss them as follows:

**1. Assignment Operators**

and the simplest one is the " = "  and in JS we assign a value for a variable. this value could be a number, String, another variable, calculation, and so on.

Here is some **Example:**
- ``` var x = 1 ```
- ``` var y += x ```
- ``` var j = 1+2 ```


**2. Comparison Operators**

This type of Operators is compares operands  and returns the logical value based on whether the Comparison is true, the type od operands could be a numbers, String, logical, and objects values. we use some notation as **( ==, != === , !== , > , >= , <, <=)**

Here is some **Example**

- ``` 
x = 3
    if(x == 3){ // means Equal
      // it will returns true
    }
``` 


- ``` 
x = 3
    if(x != 3){ // means not Equal
      // it will returns false
    }
```


- ``` 
x = 3
    if(x >= 4){ // means if it Equal or greater than
      // it will returns true
    }
```


**3. Arithmetic Operators**
and it takes numerical values as operands and then returnsa single numerical value. and in this Arithmetic we use **(addition, subtraction, multiplication, and division) as a stander Operators.**

here is some **Example:**

* ```  1 / 2; // and it's returns 0.5 
```

* ``` 1 + 3; // and it's returns 4 ```

**4. Bitwise Operators**

This Operator treats their operandsas a set of 32 bits (Zeros and ones) and not as decimal or hex or even octal numbers. 

here is some **Example**

* ``` 
15 & 9 = 9 
// in binary --> 1111 & 1001 
and the result is 1001
1001 = 9
```

**5. Logical Operators**
it's typically used with boolean values and returns the value according to the Operators used. so if the Operator used is a boolean it will return a boolean value, otherwise it will return a non-boolean value.
we use **(&& and ||) Operators**.

here is an **Example:**

* ``` exper1 && exper2 
// if both are true, it will return true. 
```

**6. String Operators**
we use the cancatenation Operator (+) and by it we can cancatenates two string values together. 

here is some **Example:**

* ``` 
var myName = 'Qamar';
myName += 'Alkhatib'; 
// and the result will be Qamar Alkhatib. 
``` 


**7. Conditional Operator**

The only JavaScript operator that takes three operands is the conditional operator. Based on a condition, the operator can have one of two values. 
**The syntax is as follows:**


* ```
 condition ? val1 : val2 
```

**8. Comma operator**
(,) returns the value of the final operand after evaluating both operands. This operator is most commonly used inside a for loop to update many variables each time the loop is run.

here is an **Example:**

``` 
for(var i = 0, j = 1; i <= j; i++, j--)
```

and we have other types such as **typeof , and unary Operators.** 

## **Loops**
Loops are a convenient and efficient technique to repeat a task. Loops come in a variety of shapes and sizes, but they all perform the same thing: **they repeat an activity a certain number of times.**

* **For Loop**
A for loop is a conditional expression that repeats until it evaluates to false.

here is its syntax:

```
for ([initialExperssion]; [conditionExperssion]; [incrementExperssion])

statement
```

* **While loop**
As long as a stated condition evaluates to true, this statement performs its statements.

here is its syntax:

* ```
while(condition){
  statement
}
```