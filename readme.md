<div style="border:solid;padding:10px;">
<span style="float:left;border:solid 1px;">Author: Andrea Zappa </span>
<span style="border:solid 1px;float:right;">
Exercise 05-css-rules
</span><br>
</div>


In this project we are gonna explain the various methods to style a webpage. We know that CSS stylesheets are needed to give a pleasant view to a webpage to the user.
So below you can learn more about this and get an idea how to implement.

 ```01-simple-styling/embedded``` folder it's showed how to style a webpage including style rules into the page, not elsewhere.
It's a bad practice and not recommended as in a real project consist of tens of pages and the developer is forced to duplicate the same rules over multiple pages.
It's better for just learning purposes.
To do that we just add the ```<style>``` element containing the css rules inside the ```<head>``` .


```01-simple-styling/external``` folder indicate the right way to link a stylesheet to a webpage. That is the better method comformed to the guidelines on web projects.
Create a CSS file and place it in a separated folder, after that in the page where we want to be styled we just add inside the ```<head>``` element the ```<link>``` with attributes that links to external css file.

```01-simple-styling/inline``` folder recreate maybe the worst case by using the inline method, including in every element the ```style``` attribute which define the style for that specific element. Avoid avoid avoid this method when the project get more larger or at least you should use when you are in "Stage" development process.
This practice lead the project becoming too difficult to manage in the future.

In ```02-simple-selecting``` folder enlighten different uses of css selectors such as Element selector like:
``` 
p {

}
```
will refer to each paragraph element in the page indifferently if it's a parent or child.
Relational selectors take in account of the hierarchy of structured html page.
In order to be applied must be separated by a space. Such technique works with elements, class selectors and ID selectors or a merge of these.
```
file: style.css
---------------
p a {
    color:white;
}
```
```
file: index.html
----------------
<p>a paragraph with an anchor element.  
    <a href=''>link to another page</a>
</p>
```

```03-font-mania``` implements many css rules found in the previous folder, additionally a new rule is used like the Pseudoclass which define the look of an element depending of its state. It means for example when you are having an  anchor element to style, you could set the appearance when it's rendered using ```element:link``` or in case the link has been visited ```element:visited```, the browser save its state of "link visited" until a refresh has been done. Another one the hover state ```element:hover``` take effect when the cursor is placed upon the anchor.

```04-font-reset``` inside there are shown three different methods to reset css properties of specific elements to a base setup. It mean that depending of level of reset a webpage can be reset in a way that almost the newest browsers shows the same result, here for example the ```test-destyle``` acts like a drastic reset as noticed when you open the page.
The level of reset get more aggressive, the more efforts must be taken in account when you are styling.
