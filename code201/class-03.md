## Continuing Jon Duckett HTML,CSS and JS book:

# Chapter 3 - Lists

in this chapter, Duckett has summarized the lists into three different types:

1. ordered lists, and each item in this list will be numbered by (numbers, characters..etc) and we use these HTML tags(<ol> and <li>).

- Code Example:

```
< ol>
  < li>Mix flour, baking powder, sugar, and salt.< /li>
  < li>In another bowl, mix eggs, milk, and oil.< / li>
  < li>Stir both mixtures together.< /li>
  < li>Fill muffin tray 3/4 full.< /li>
  < li>Bake for 20 minutes.< /li>
< /ol>
```
2. Unordered list, and in this list its begin with a bullet point and not numbers or characters. we use these HTML tags (<ul> and <li>)
- Code Example:


```
< ol>
  < li>first item< /li>
  < li>second item   < /li> 
    < ul>
      < li>second item first subitem< /li>
      < li>second item second subitem< /li>
      < li>second item third subitem< /li>
    < /ul>
  < /li>        
  < li>third item< /li>
< /ol>

```
3. Definition lists and this list are made up of a set of terms along with the definitions for each of those terms. we use these HTML tags (< dl>, < dt>, < dd>).

- Code Example

```
< dl>
< dt>Sashimi< /dt>
< dd>Sliced raw fish that is served with 
 condiments such as shredded daikon radish or 
 ginger root, wasabi and soy sauce< /dd>
 < dd>An Italian cheese usually made from whole 
 cow's milk (although it was traditionally made 
 from buffalo milk)< /dd>
< /dl>

```

# Chapter 13 - Boxes
This chapter talks about CSS boxes and we have dimensions(width, height), and we can limit the width and height with (max-width, min-width, max-height, min-height). And talk about the overflowing content(when the content is contained within a box is larger than the box itself), ANd talk about Border, Margin, and padding. Border, and its style and color, and how to do shorthand border. How to move the box to the center. And in CSS3, how to add images t the border, Box shadows.

## JavaScript chapters.
# Chapter 2- basic JS instructions

is talking about arrays, and how to create an array. and what values we can use inside it, and how to access it and change the value here is a code example to creating an array:

```
var fruits;
fruits = ['Banana', 'Apple','Watermelon' ]

```

# Chapter 4 - Loops

its talk about the truthy & falsy values, Also talk about the types of loop and how to use them:

1. For loop, Code Example:

```
 for (let i = 1; i <= 5; i++){
     document,write(i);
 } 
```

2. While loop, code Example:

```
 While(condition is true){
     do something
 }
 ```

3. Do while, Code Example:

```

 do{
     //do something
 } 
 while(condition is true)
     //do something

```
