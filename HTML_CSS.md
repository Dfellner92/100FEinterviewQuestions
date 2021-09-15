### Name some CSS properties

Some to talk about: ```font-weight```, will allow you to make font thinner or bolder, ```font-size``` to change the pixel value. ```margin``` is used to create space outside of defined borders, ```padding``` is used to create space within defined borders, ```border``` can change the dimension of the borders, and each of these can be specified in terms of direction. ```display``` which could make an element displayed inlined with the rest of the row or blocked which gives it a new row, ```position``` which allows for absolute positioning, to fix an element relative to its first positioned parent. ```box-sizing``` will allow for a border box to account for borders of other elements to fix its size accordingly.

### visibility: hidden v display: none

if you had 2 150x150px divs on top of each other, the top green and the bottom red each with its own id for background-color, you could apply ```visibility: hidden``` on the green and it'd keep the red div in place as it simply looks invisible with its height and width still applied. However, ```display: none``` will make it appear as if the div has disappeared altogether, and the red div would move up in its place.

### CSS terminology

A CSS file typically contains defined ```selctors``` (id, classes, and tags within the HTML) The selectors contain ```properties```, which cause the selector to alter, usually specified by the property name. The way the properties are altered is through assigning them a ```value```. For example we could have the property font-height: and give it the value 20px. Together, the property and its value form a ```declaration```. Together, all the declarations of selector class form the ```rules```

### Data attributes

### class vs id

a class is denoted by the ```.``` prefix, an id is denoted by the ```#``` prefix. id is meant to be more specific than a class, used only for one (although you could use it for more than one but most would consider this bad practice) Due to id having a higher specificity, it can overwrite class styles.

### CSS specificity

CSS specificity deals with what selectors get applied to certain elements based on inheritance. If you had a ```*``` (universal selector), with a ```color: red``` declaration, it'd be overruled by the color declaration of an h1 selector. That would be overruled by the class selctor, which would be overruled by the id selector, and then the most specific would be inline styling. 

### responsive design

Media queries allow us to have breakpoints in the browser width that allow for style changes. There is also the more outdated bootstrap 12 column grid, but now CSS flexbox allows us to have these dimensions built in natively.

### CSS box model

The box model is how certain properties work around each element. It begins with the element, the padding surrounding it, then the border, then the margin, which moves it away from other box models.

### CSS preprocessors

Why would you use a preprocessor like SASS? It allows for variables and nesting of variables which allow for cleaner code. Being able to see the scope helps legibility. Mixins allow for code to be reused much easier as rules can be added to new selectors much quicker and cleaner.

### Pseudo class

Additional selector type that orders elements around pages or affects user interactions. Pseudo classes are denoted by the colon in front of various classes like ```hover```. They can also be used to make every nth row colored differently, for instance.

### Pseudo elements

### Create a circle

Create a div with an id selector ```#ciricle``` attached to it. In the stylesheet, create a selector class that gives #circle background-color of red, height: 100px, width: 100px; and finally, a border-radius of 50%.

### semantic HTML

Semantic elements were introduced in HTML5 with the aim to have more specific tag names that would replace id selector conventions that had become standardized. These included ```<div id="footer">``` or ```<div id="section">``` and are now replaced with ```<nav>``` and ```<footer>``` tags. These better named containers help improve workflow as well as SEO.

### head tag

The head tag is used to store external dependencies in a ```.html``` file, like a stylesheet or a script file. It also is used to store ```<meta>``` tags that contain information about the title, if you're going to allow responsive functionality, containing SEO and more. It should be worth noting that the head tag doesn't render any features to the DOM.

### meta tags

```<meta charset="UTF-8">``` is used to define the characters we're using. ```<meta description="my seo here...">``` is where the SEO keywords can go, you could also use ```keyword=" "```. ```<meta name="viewport" content="width=device-width, initial-scale=1.0">``` is a very common tag that frames the users view of the content. ```width``` controls how the view is scaled for the device used, and ```initial-scale``` indicates that we're not zooming in. 