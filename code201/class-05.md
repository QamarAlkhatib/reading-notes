## Continuing from Duckett HTML&CSS, and JS book.

# Chapter-5 images

This chapter talks about how to add images to the web page using HTML. In HTML we have a tag for an image, and when adding an image we use this syntax:

```
<img src="image link" alt="description about the image" title="to add more info about the image" />

``` 

also, the image place will be placed according to the code placed in the HTML.


# Chapter-11 Color

This chapter talks about the colors in CSS and the way we add them to our page. We have three types of foreground color:
1. RGB values, we can apply it as:


```
color: rgb(30,30,60);
```

2. HEX codes, we can apply it as :

``` 
color: #ee3e80;

```

3. Color names, we can apply it as:

```
color: blue;
```

we can add also a background color using (background-color). 
in CSS3, there is called opacity, and this allows you to specify the opacity of an element and any of its child elements.

```
opacity: 0.5;

```

# Chapter-12 Text

This chapter talks about the different types of text and the way we can change it in CSS. This image gives you a brief understanding of the text:

![](images/text.png)


# Blog post JPEG vs PNG vs GIF

**JPEG** is a lossy compression standard that capitalizes on human perception. It can achieve compression ratios of 1:10 with no noticeable quality loss. Compression artifacts become more noticeable after that. also, it doesn't support transparency.

**PNG** is a lossless picture format that uses the DEFLATE data compression. During compression, no data is lost, and no compression artifacts are added to the image. As a result, a PNG picture will preserve greater quality than a JPEG image and will appear much sharper. also, it supports transparency.

**GIF** is a lossless picture format that uses the LZW algorithm for compression. In its early days, it was preferred over PNG for basic graphics in websites since PNG's popularity was still rising. also, it supports transparency by a single color.