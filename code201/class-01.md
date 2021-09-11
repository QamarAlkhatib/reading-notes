## Summarizing my reading from Duckett HTML book:

### **introduction**

The name of the book is HTML & CSS (DEsign and build websites) For Jon Duckett. 
in the first few pages, he says that it's not that hard to learn how to write web pages and read the code used to create them, And he assures that his book will help anyone who wants to learn to create web pages or even to understand HTML & CSS in an easier way.

On page 6 of the book, Jon Duckett divided the book into three sections in order to learn to create web pages, And they are as follows:

**1: HTML**
in the first chapter, we will look into how HTML is used to create web pages by writing what we want, and then using tags or elements to the words like the header and the body and paragraph. as well as where it starts from it where its ends. All of these For the browser.

**2: CSS**
Jon Duckett wanted to start with a chapter that explains how CSS uses rules to make you in control with styling and layout for the web pages. and then we will look into the CSS properties with its two types, **presentation** and it gives you how to control things like the color of the text, the font, the background colors, and how to add background images. and the other type is the **layout** and it teaches you how to control where the different elements are positioned on the screen.

**3: Practical** 
In the end, the book will introduce HTML5 to help describe the structure of the web page. And will end up looking at SEO( search engine optimization).

## How People Access The Web

1. we have **Browsers**, and it's a software called web browser such as, google chrome, safari, and opera. In order to view a web page, 
users might type a web address into their browser, follow a link from another site, or use a bookmark. Software manufacturers regularly release new versions of browsers with new features and supporting new additions to languages. 

2. **web servers** and are private computers that are constantly connected to the Internet, and are optimized to send web pages to people who request them.

3. **screen readers** These are programs that read the contents of the user's computer screen. Commonly used by people with visual impairments.

4. **devices**
People are accessing websites on a growing range of devices including desktop computers, laptops, tablets, and mobile phones.

## How Websites Are Created
 All the websites are created from HTML and CSS but there are other changes in the content management system or blogging software etc. platforms add a new few more technologies.
 This section is divided into three sections, as follow:

 1. **What we see on a web page**
 When looking at a website, the browser will be receiving HTML and CSS from the web server that hosts the site. most web pages include extra content such as images , videos, or animations.

 2. **How it is created**
 Small websites are often written in HTML and CSS Just. and larger websites that use content management systems or blogging tools are often more complex of different technologies on the webserver. and larger--> more complex sites like who use the database, other programming languages such as PHP, ASP.net, Java and so

 3. **HTML5 & CSS3**
 there are several versions of HTML and CSS and each one is improved from other previous versions. 

##  How The WebWorks

When visitors visit a website, the webserver that hosts it might be located anywhere on the planet. The browser will initially connect to a Domain Name System (DNS) server to determine the location of the webserver. the steps of how the web works are as follows:

1. **A visitor connected to the web via the internet service provider, the visitor most likely wrote the domain name or the web address into the browser to visit the site**

2. **The visitor computer connects to the network server which is the DNS (Domain name servers) and the DNS tell the visitor computer the IP address with the requested domain name**

3. **The IP Address is a unique number, and the DNS return it to the visitor computer to allows the browser to connect to the webserver that hosting the website (The visitor requested)**

4. **After that The web server sends the page that the visitor requested back to its browser**  

# Chapter 1 - HTML Structure

Structure is critical in assisting readers in comprehending the messages you're attempting to express as well as navigating the text.

## How Pages Use Structure
When reading a news piece online, the format is fairly similar (although it may also feature audio or video).

## Structuring Word Documents
In any text, the use of headings and subheadings frequently indicates a hierarchy of information. This may be elaborated on in the subheadings farther down the page. When creating a document with a word processor, we divide the text to give it structure. Each part can include a title that describes what it covers, and each topic can have its own paragraph.

## HTML Describesthe Structure of Pages
The HTML code below is made up of HTML elements, which are characters that exist inside angled brackets. An element is made up of two tags: an opening tag and a closing tag, in most cases. (There's an additional forward slash in the ending tag.) Each HTML element provides information to the browser about the information contained between its opening and closing tags.

``` 
<html>
<body>
 <h1>This is the Main Heading</h1>
 <p>This text might be an introduction to the rest of 
 the page. And if the page is a long one it might 
 be split up into several sub-headings.<p>
 <h2>This is a Sub-Heading</h2>
 <p>Many long articles have sub-headings so to help 
 you follow the structure of what is being written. 
 There may even be sub-sub-headings (or lower-level 
 headings).</p>
 <h2>Another Sub-Heading</h2>
 <p>Here you can see another sub-heading.</p>
</body>
</html>
```

Also HTML use Elements to describe the structure of pages:
![](imags/HTML.png)


### The Tags are consists of:
- HTML opening Tags:

![](images/tags.png)


- HTML Closing Tags:
![](images/tagcl.png)


## The Attributes for elements
Attributes are used to offer additional information about an element's contents. They are made up of two parts: a name and a value, separated by an equals sign, and occur on the element's beginning tag.

here is an Example:

![Attribute Example HTML](images/attH.png)

## Body, Head & Title:

*a quick description*

1. **<body></body>** everything inside this element is shown inside the main browser window.

2. **<head></head>** often this comes before the body element and this contains information about the page.

3. **<title></title>** usually this element inside the head element, and the contents of title elements are shown in the top of the browser (where we usually typle the URL of the page) or in the tab for that page.

in this picture you will find the summery structure from Jon Duckett book:

![summery structure](images/summarySt.png)


# Chapter 8 - Extra Markup

## The Evolution of HTML

* HTML4 *released 1997* : The elements that were seen in this book, with the exception of a few elements added in HTML5 (which have been marked), were all accessible in HTML 4. Despite the fact that HTML 4 included certain presentational elements for controlling the look of pages, authors are no longer advised to utilize them.such as **< center> element, < font>, and < strike> etc.**

* XHTML 1.0 *released 2000* : The XML language was first released in 1998. Its goal was to make it possible for individuals to create new markup languages. Because HTML was the most frequently used markup language, it was determined that HTML 4 should be rewritten to conform to the XML requirements and renamed XHTML. This meant that authors had to adhere to certain new, more stringent markup standards. Consider the following scenario:
    1. Except for empty elements like image />, every element required a closing tag.
    2. The attribute names had to be in lowercase
    3. All attribute required a valueand the values must be in double quotes.
    4. Elements that have been deprecated should no longer be utilized.
    5. Every element that has been opened within another element should be closed within that element. 

    - Two major versions of XHTML 1.0 were produced to assist web page authors in transitioning to this new syntax:

    1. **Strict XHTML 1.0**, which required writers to strictly adhere to the standards.

    2. **Transitional XHTML 1.0**, which allowed writers to keep presentational features like center and typeface.

* HTML5 *released 2000* : HTML5 eliminates the necessity for web page authors to close all tags, and new elements and attributes are introduced. The HTML5 standard was not yet complete at the time of writing, but major browser makers had begun to integrate many of the new capabilities, and web page authors were quickly embracing the new syntax.

# DOCTYPEs
Because there have been multiple versions of HTML, each web page should begin with a DOCTYPE declaration that informs the browser which version of HTML it is using (although browsers usually display the page even if it is not included).

- here is a picture that shows the difference of writing the doctype in HTML5,4 XML, Transitional and Strict XHTML:


![](images/doctyps.png)


# Comments in HTML
You may use the text between these characters to add a comment to your code that will not be shown in the user's browser:
``` <!-- comment goes here --> ```

It's a good idea to include comments to the code because, no matter how knowledgeable you are with the page at the time of creating it, comments will make it much easier to understand when you come back to it later (or if someone else needs to look at the code).

# ID Attribute

The id property can be applied to any HTML element. It's used to distinguish that element from the rest of the page's elements. It should be preceded by a letter or an underscore (not a number or any other character). It's critical that no two items on the same page have the same id attribute value (otherwise the value is no longer unique)
Because it may be used on any element, the id property is known as a global attribute.

* here is an example, The code and the result of using id Attribute:

![](images/Idattribute.png)

# Class Attribute
A class attribute can be applied to any HTML element. Rather of identifying a single element inside a document, you may need a means to distinguish many components as being distinct from the others on the page.

* here is an example, The code and the result of using class Attribute:

![](images/classattribute.png)

# Block Elements
In the browser window, some items will always seem to begin on a new line. Block level elements are what they're called. h1>, p>, ul>, and li> are examples of block elements.

* here is an example, The code and the result of using block element:

![](images/blockelements.png)

# inline elements
Some elements will always appear to continue in the same direction as their neighbors. Inline elements are what they're called. a>, b>, em>, and img> are examples of inline elements.

* here is an example, The code and the result of using inline element:

![](images/inlineelements.png)

# Grouping Text & Elements In a Block
You may use the element to aggregate a number of elements into a single block-level box.
For example, you might build an element that contains all of the elements for your site's header (logo and navigation), or you could create an element that contains visitor comments.
The contents of the element will start on a new line in a browser, but it will have no effect on the page's display. Using an id or class property on the element, on the other hand, allows you to set CSS style rules that specify how much screen space the element should take up and how the appearance of all the components included within it should be changed.

* here is an example, The code and the result of using Grouping Text & Elements In a Block element:

![](images/groupblockelement.png)

# Grouping Text & Elements Inline
The span> element serves as an inline replacement for the div> element. It can be applied to:

1. Include a portion of text with no other acceptable element to distinguish it from the rest of the text.

2. Have a lot of inline components.

The most common reason for utilizing span> elements is to utilize CSS to alter the look of the content of these elements.

* here is an example, The code and the result of using Grouping Text & Elements Inline element:

![](images/inlinegroupingelemetn.png)

# IFrames
An iframe is a little window that has been sliced into your page, and it allows you to see another page via it. The acronym iframe stands for inline frame. The embedding of a Google Map onto a page is a frequent usage of iframes (which you may have seen on many websites). Any html page (on the same server or elsewhere on the web) can be used as the iframe's content.

* here is an example of using Iframes and the result:

![](images/iframes.png)


The iframe> element is used to construct an iframe. To utilize it, you'll need to understand a few characteristics:

1. **src** The src property gives the URL of the frame's content.

2. **height** The iframe's height in pixels is specified by the height property.

3. **width** The width property defines the iframe's width in pixels.

4. **scrolling attribute**  HTML5 will not support the scrolling attribute. It specifies whether or not the iframe should contain scrollbars in HTML 4 and XHTML. If the page inside the iframe is larger than the space you've set aside for it, this is crucial (using the height and width attributes). Scrollbars allow the user to navigate around the frame in order to see additional information.

5. **frameborder** HTML5 will no longer support the frameborder attribute. It specifies whether or not the frame should be bordered in HTML 4 and XHTML. If the value is 0, no border should be displayed. A border should be displayed if the value is 1.

6. **seamless** Where scrollbars are not wanted, an iframe can be given the seamless attribute in HTML5. Although the seamless attribute (like several other new HTML5 attributes) does not require a value, it is frequently used by developers. The seamless attribute does not work in older browsers.

* continue the example of iframe characteristics:

![](images/Iframe2.png)

# Information About Your Pages

* The **< meta>** element is contained within the element and contains data about the web page. It is not visible to visitors but serves a variety of functions, including informing search engines about your page, who produced it, and if it is time sensitive. (A page can be configured to expire if it is time sensitive.) Because the element is empty, it does not have a closing tag. The http-equiv and content attributes are also used in pairs in the meta> element.

* **description** This is where you'll find the page's description. This description, which should have a maximum of 155 characters, is often utilized by search engines to comprehend what the page is about. It's also sometimes seen in search engine results.

* **keywords** This section contains a list of comma-separated keywords that a user can use to locate the page. In reality, this has no visible impact on the way search engines index your site.

* **robots** This tells search engines whether or not to include this page in their results. If you don't want this page to be added, use the value no index. If you want search engines to index this page but not the pages it links to, use the no follow option.

* **author** This defines the author of the web page.

* **pragma** This prevents the page from being cached by the browser. (That is, downloading it once and keeping it locally to save time on later visits.)

* **expires** Because browsers frequently store a website's content, the expires option can be used to specify when the page should be removed from the cache (and no longer be cached). It's important to note that the date must be entered in the manner provided.

- here is an example of using meta:
![](images/meta.png)

# Escape Characters
HTML code makes use of and reserves a number of characters. (Take, for example, the angled brackets on the left and right.) As a result, you must use "escape" characters if you want these characters to show on your website (also known as escape codes or entity references). To create a left angled bracket, for example, you may use either &lt; or &#60;. You can use either &amp; or &#38; for an ampersand.

* list of escape codes:
![](images/codeesc.png)

- Summary for chapter 8:
![](images/ch8summary.png)


# New Html5 Layout Elements 
HTML5 introduces a new set of elements that allow you to divide up the 
parts of a page.
most likely the pages like this:
![](images/HTML5.png)

* The elements header> and footer> can be used for:

1. The site's primary header or footer, which displays at the top or bottom of each page.

2. An separate article> or section> within the page's header or footer.

* **Example**

![](images/headerandfooter.png)

* **navigation** The nav> element is used to hold the site's important navigational blocks, such as the main site navigation.

* **Example**

![](images/nav.png)

* **artical** The article> element serves as a container for any part of a page that may stand alone and be syndicated.

* **Example**

![](images/artical.png)

* **asaide** 
Depending on whether or not it is inside an article> element, the aside> element serves two purposes.

* **Example**

![](images/aside.png)

* **Sections** The section> element groups together related content, and each section usually has its own heading.

* **Example**

![](images/sections.png)

* **Heading groups** The hgroup> element's purpose is to group together one or more h1> through h6> elements so that they are treated as a single heading.

* **Example**

![](images/headinggroup.png)


* **Linking Around Block-Level Elements** HTML5 allows web page authors to wrap a block level element with child elements in an a> element. This allows you to make a link out of an entire block.

* Summary:
![](images/summary17.png)

# chapter 18 - Process & Design
This chapter is talking about the Target Audience and some useful questions to answer them to know who is the target for this website, and we have individuals and companies as a target audience.
and before we doing the website, we must take under consideration why people want to visit my website as well as we must ask ourselves, what my visitor is trying to achieve. And, for the content, we must ask What information my visitor are looking for/need. How often people will visit my site, All of these questions help the individual to choose their target audience carefully, and these questions help the user who wants a website to know if he/she is on the right track with a good idea that people might need it in the future.


After that, he/she can produce the next step which is creating a site map, and it looks like this:

![](images/sitemap.png)

and then creating a wireframe for the website, and it looks like this:

![](images/wireframeEx.png)


Summary for chapter 18:
![](images/summary18.png)



# reading JavaScript from Jon Duckket

## What is A script and How Do I Create One?

* A script is a set of instructions that a computer can use to accomplish a specific task. 
 A browser may use different parts of the script depending on how the user interacts with the web page, Also, scripts can run different sections of the code in response to the situation around them.


 ### writing a script:
 To write a script we need to state our goal and then list the tasks that need to be completed in order to achieve it.


### designing a script: Task once we define the goal of the script, we can work out the individual tasks needed to achieve it. 
In this picture a view of tasks was made by flowchart:

![](mages/taskflowchart.png)


### designing a script: steps

each previous individual task may be broken down into many steps, and these steps can then be translated into individual lines of code.

* here is an Example:

![](images/scriptsteps.png)


### Now these steps to code

Every step for every task shold be written in progrmming language so can the computer understand it.

Summary of The ABC of programming:

![](images/ABCsuammary.png)


# How do computers fit in with the world around them?

## OBJECTS & PROPERTIES
Every physical thing in the world can be represented as an **object** in computer programming.

Each **property** has a name and a value, and each name/value pair provides information about the object's individual instances.


## Events:
People interact with objects in the real world. These interactions have the potential to alter the values of these objects' properties.

## Methods:
Methods represent the actions that people must take with objects. They have the ability to get or change the values of an object's properties.

## And When Adding all of the togther:
Data is used by computers to create models of real-world objects.
An object's events, methods, and properties are all linked together:
Methods can be triggered by events, and methods can retrieve or update the properties of an object.

- web browser are programs built using objects.

## THE DOCUMENT OBJECT REPRESENTS AN HTML PAGE 
You can use the document object to change and access the content that users see on the page, as well as respond to how they interact with it.

