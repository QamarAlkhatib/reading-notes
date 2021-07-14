
## based on what I've learned on today's class for Javascript

### 1. Js Intro Paragraph 

A web server is a special computer connected to the Internet that is optimized to send web pages to people who request them. **JavaScript is a scripting language that can affect HTML elements in the form of images, layers, paragraphs, etc., as well as some non-HTML objects in the browser window.**

Most websites send JavaScript code to your browser to make the site interactive. When **the user receives a page that contains JavaScript, the JavaScript interpreter jumps in the user's browser and tries to execute the JavaScript. The browser executes the JavaScript code while the page is loading and the user interacts with the page.**

**JavaScript commands allow you to write information on a web page, and you can place a < script > tag anywhere on the web body where a script should write its message.** *In many cases,* you can insert the **opening and closing script tags** into the page header to organize your **JavaScript** code in an area of the page. In fact, it is common to include the 
```< script > ``` tag in the closing tag, as this **ensures that the visitor can see that the page is running JavaScript when the page is loaded.**


### 2. . Input and Output in JS

The traditional output of JavaScript is an alarm message, so you can get alerts from anywhere in the world. The warning message appears in a pop-up window in the JavaScript browser, but it is important to understand that the warning function itself is not part of JavaScript. It is given to you by the browser, so if you try to execute an alarm on a node, it is not the case that there is no pop-up box on the node.

* **And we can do the alarm message by"**

``` alarm("Some message") ```

* **we can define a variable and assigning a value to it by:**

``` var x = 10 ```

* **OR to a String value**

``` var y = "String Value" ```

* #### And we can use to print X or Y **but not to the user**

``` console.log() ```

* #### we can use this one for the user to take the input
``` promot(Enter Name) ```

### 3. Variables In Js
**JavaScript variables are case sensitive**, for example there are several variables. **JavaScript variables have a type, i.e. A variable can contain a value of any type of data.**

You can assign a value to a variable using the **equals operator**, or you **can declare a variable and use it**. JavaScript contains variables that contain **data or values**, and the **data or values can be changed**. If the value or type of a variable changes during program execution, JavaScript will take care of it.