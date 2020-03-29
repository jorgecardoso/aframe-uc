---
title: Intro to HTML
---

# Intro to HTML and A-Frame

## HTML
HTML is the language to create web pages and it is the language we will be using to create Virtual Reality worlds that run on web pages.

An example structure of a web page is:

```html
<!DOCTYPE html>
<html>
   <head>
      <title>HTML Basics</title>
   </head>
   <body>
      
   </body>
</html>
```

HTML is based on *tags*. A tag is a word written between the symbols `<` and `>`. Tags are usually used in pairs of *starting* tags and *ending* tags. Notice, for example on the `<title>` stating tag and the `</title>` ending tag.
The starting and ending tags delimit an HTML *element*. The title element, for example defines the title of the web page (the text your browser shows in the tab of the web page).

Elements (things between a starting and ending tags) can be nested -- they can have other elements inside them. Notice for example, on the *head* element: it has a title element and a script element inside of it. The head element is where we define the title of the web page and where we load scripts of code that the browser will execute on the web page.

The most important element in a web page is the *body* -- delimited by the `<body>` and `</body>` tags. Everything inside the body is considered the content of the web page.


1. Go ahead and locate the file for example `00-intro-01` and add the following line of code inside the body and then preview the file on your browser:


```html
<h1>This is a web page</h1>
```


## A-Frame

A-Frame is a set of HTML elements that the browser will render as 3D objects in an interactive virtual environment.

A-Frame needs a special script for this (needs to be put inside the `head` element):

```html
<script src="https://aframe.io/releases/0.8.2/aframe.min.js"></script>
```

The main content element of A-Frame is the scene element - `<a-scene>` - it delimits the content of our virtual world:

```html
<!DOCTYPE html>
<html>
   <head>
      <title>HTML Basics</title>
      <script src="https://aframe.io/releases/0.8.2/aframe.min.js"></script>
   </head>
   <body>
       <a-scene>
        <a-box color="blue" position="0 1.6 -2"> </a-box>
      </a-scene>
   </body>
</html>
```

Inside a scene we put other elements that represent 3D objects.

In the above example, we have used the element `a-box`. Notice that inside the starting tag we have added attributes and values that describe the `a-box`. Attributes are `name=value` pairs written inside the starting tag:

```html
<a-box color="blue" position="0 1.6 -2">
```

In this case the `color` attribute has the value "blue" and the `position` attribute has the value "0 1.6 -2".


1. Locate example `00-intro-02` and change the color attribute to `red` and preview the changes.