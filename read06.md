## based on what I've learned in today's class for class

## 1. CSS
**Cascading Style Sheet (CSS)** is a style sheet language used to describe the presentation of documents written in a markup language such as HTML. It sets the **background color, font size, font family and color properties of elements in a web page.** The name "cascading" comes from the fact that a priority scheme is set to determine which style rules should apply and whether more than one rule should fit a particular element. 

Style sheets contain **rules for page layout, formatting, color, fonts, and other style information for individual elements such as text.** External stylesheets are stored as CSS files and used to determine the appearance of an entire web site in a file, rather than adding instances of CSS for each HTML element you want to customize. Link a file to your external stylesheet (in this case mysitestyle.css) and the CSS instructions it applies to your links on the page.

## 2. How To add CSS  
by Three ways:

* **Inline style such as:**

``` <p style="color.blue"> <p> ```

* **internal style such as:**

```  
<head>
<style>
p {
  color:blue
}
</style>
</head> 
```

* **External style such as:**

    
1.  create a **CSS** file by

 ``` style.css ```


2. link with the HTML file by:

``` <head> <link rel="stylesheet" type="text/css" href="style.css"> </head>```


## 3. CSS Color
The most common way to specify colors in CSS is to use hexadecimal values. Hex codes are bytes with values from 0.0 (the color with the lowest intensity) to FF (the highest intensity).

**We use hex , RGB , color name , hue etc**

## 4. CSS Reference

1. **Padding** is the distance between the content and the edge of an element. By default, the browser calculates the width of the element and applies the calculated width to the height of the content area, taking into account the padding and the border area. We can adjust these values in CSS to bring the boundary closer to the content.

2. **Selectors** are used in CSS to select parts of the HTML style. You can use multiple selectors for exactly the item you want to use (parental nesting). You can change inline elements so that they are blocked, or block elements so that they are inline without changing the Display: CSS property.

3. **background-color**

4. **background-image**

5. **Color**

6. **margin**
 
7. **text-align**


## 5. Myers Web Reset Stylesheet
Cascading Style Sheets (CSS) are better suited to the presentation of documents in the markup language HTML. In Undo, **Eric Meyer explains why your web browser displays HTML markup the way it does.**

The process is quite complex regarding the use of Cascading Style Sheets (CSS) for better cross-browser compatibility and requires additional attention to the specifics assigned to the programming language. Simply put, using CSS Reset for better cross-browser compatibility allows the developer to format multiple websites. The developer can specify the different styles for different default browser settings applicable to the project web page.
   


