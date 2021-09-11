## Continuing from Duckett JS book

# Chapter 3 - Object Literals 
this chapter talk about objects and object Literals. THe object Literals is the easiest and most pupular way to create objects 
- Creating an object using literal notation

```
var hotel {
    name: 'h1',
    rooms: 5,
    booked: 3,

    checkAvailability: function(){
        return this.rooms - this.booked;
    }

}
```

we can access the properties or methods of an object using dot notation **.**

# Chapter 5 - DOM
 The document object model (DOM) specifies how browsers should create a model of an HTML page and how javascript can acess and update the contents of a we page while it is in the browser window. 
 - The Dom tree is a model of a web page:
 here is an example:
 ![](images/dom.png)