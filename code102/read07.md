### based on what I've learned in today's class for Functions in JS

# Functions
we can define the Javascript functions as it's a block of codes that preform a specific Task. and it's executed when we call it. 

We have two-way to define a function as below: 

1. ``` 
function FunName(myName){
  console.log("My Name is, ${myName}); 
}
FunName() //we call it like this, by it's name
```

2. ```
var myName = function(name){
  console.log("Hi " + name);
}
myName() //we call it like this, by it's name
```

And we have a Return statement in a function,
which return one value of that function, Like this Example:

```
var y = sum(1,2);
Function sum(i,j){
  return i+j;
} // the result = 3
```
## The advantages of functions: 
* Code readability. 
* Code reusablity because we only define the code once and we can use it many times.

* It help to avoid repeated code.


To see about the Expressions and operators in Javascript [Check this link out](https://qamaralkhatib.github.io/reading-notes/read05). 


# Control flow
### Overview; 
We can use conditional statements to write programs using control flow. 

### Control flow: 
The control flow is the sequence in which a script's statements are executed by the computer. **Unless** the computer detects (very common) structures that affect the control flow, such as conditionals and loops, code is executed in order from the first line in the file to the last line.

here is an Example:
in my [website](https://qamaralkhatib.github.io/SpaceCraft/)
 I created some **Control flow** 
for the user using **while loop** ,
here is what I did:

``` 
var picNum = prompt("How many photos you would like to see for " + favCom + " Rocket ?")

while(picNum > 10){

 picNum = prompt("Oh,That will crash my website :(, Please Enter a number equal or less than 10!")
}
```
This code tells the user to enter how many pictures he wants to see for the specific company rocket, and if he entered a large number the message will show again until the user enter the right value. 

and by control flow, we control on the user based on his/her input.

To go back to the main page, [Click here](https://qamaralkhatib.github.io/reading-notes/)