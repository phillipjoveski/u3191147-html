# CSS 1: CSS Fundamentals



## Introduction

- Why is it called CSS?
- Basic syntax 
- Targeting elements
- Basic properties



## Why CSS?

Stands for: **Cascading Style Sheets**  

- Styles cascade from the top to the bottom
- Styles added later can override ones from the top

Works internally as well  

- If you include the same property twice, the latter one will be used



## Syntax
![Syntax](./images/css-1-1.png)



![Syntax](./images/css-1-2.png)


## Classes and IDs
In order to be able to target individual elements on the page, you can add a class or an id to a HTML tag:

ID: `<h1 id="logo">My website</h1>`

Class: `<li><a href="index.html class="currentpage">`

Then in your CSS, you can target those elements like so:

ID: 
```
#logo {
    color: red;
}
```

Class: 

```
.currentpage {
    color: red;
}

```

**Rules**

As usual, a few important rules:

*   You can make up the class and ID, but
*   You can't give a class or ID the same name as a html tag (e.g. `class="body"`)
*   You can only use the same ID once on a page
*   You can reuse a class multiple times on the same page - this is the power of CSS!

!!! important
    Note that, just because you can easily add a class or ID, it doesn't mean you should! Look at the tag structure and see if you can target it easily without having to add any classes. 



## Linking to your CSS file

The link to your stylesheet should look like:

```
<link rel="stylesheet" href="assets/css/styles.css">
```

*	It will go in the `<head>` of the html page
*	The file should be saved in the `css` folder, which is inside the `assets` folder
*	All file names and folder names are in **lowercase** and **no spaces**




## CSS reset

In addition to your primary CSS document, you'll also have use a CSS reset file. 

**Why?**

Each browser has different default styles built in, but they aren't consistent.




### Why?

As Chris Coyier (of CSS Tricks) [explains](https://css-tricks.com/reboot-resets-reasoning/):

>the whole idea of a CSS reset is to deal with styling inconsistencies across browsers. For example, just now I popped a `<button>` onto a page with no other styling whatsoever. Chrome applies `padding: 2px 6px 3px;` - Firefox applies `padding: 0 8px;`. A CSS reset would apply new padding to that element, so that all browsers are consistent about what they apply. 




### Two main options

Eric Meyer’s reset:
[http://meyerweb.com/eric/tools/css/reset/](http://meyerweb.com/eric/tools/css/reset/)

Normalize.css:
[http://necolas.github.io/normalize.css/](http://necolas.github.io/normalize.css/)


## Don't use
Inline styles. You need to ensure you keep your content in your HTML files and anything that controls the visual appearance must be in your CSS file. 

Inline CSS example:

```
<body style="background-color: red; text-align: center;">
```

That's bad, don't do it. Instead just put it in your CSS file:

```
body {
    background-color: red; 
    text-align: center;
}
```



## Have a go

*	We will create a CSS file
*	Save it in the correct location
*	Link to it from our HTML page
*	Do the same with a reset file
*	Write some basic styles


