# Brief HTML



You can use an id to style a single element and later you'll learn that you can use them to select and modify specific elements with JavaScript.

id attributes should be unique. Browsers won't enforce this, but it is a widely agreed upon best practice. So please don't give more than one element the same id attribute.
```
<h2 id="cat-photo-app">
```
```
  <form action="/submit-cat-photo">
    <label><input type="radio" name="indoor-outdoor" checked> Indoor</label>
    <label><input type="radio" name="indoor-outdoor"> Outdoor</label><br>
    <label><input type="checkbox" name="personality" checked> Loving</label>
    <label><input type="checkbox" name="personality"> Lazy</label>
    <label><input type="checkbox" name="personality"> Energetic</label><br>
    <input type="text" placeholder="cat photo URL" required>
    <button type="submit">Submit</button>
  </form>
```

# Basic CSS 

* Padding : An element's padding controls the amount of space between the element's content and its border.

* Margin : An element's margin controls the amount of space between an element's border and surrounding elements. If you set an element's margin to a negative value, the element will grow larger.

* Relative units, such as em or rem, are relative to another length value. For example, em is based on the size of an element's font. If you use it to set the font-size property itself, it's relative to the parent's font-size.

* classes will override the body element , the order of the class declarations in the <style> section is what is important. The second declaration will always take precedence over the first.

* browsers read CSS from top to bottom in order of their declaration.

*  id declarations override class declarations, regardless of where they are declared in your style element CSS.  inline styles will override all the CSS declarations in your style element.

* In many situations, you will use CSS libraries. These may accidentally override your own CSS. So when you absolutely need to be sure that an element has specific CSS, you can use !important

* Let's go all the way back to our pink-text class declaration. Remember that our pink-text class was overridden by subsequent class declarations, id declarations, and inline styles.


```
<h1 id="orange-text" class="pink-text blue-text" style="color:white;">Hello World!</h1>

```

These may accidentally override your own CSS. So when you absolutely need to be sure that an element has specific CSS, you can use !important

**css html**

```
<h2 style="color:blue;">CatPhotoApp</h2>
```

**css style in html**
```
<head>
    <style>
        h2 {
            color: red;
        }

        p {
            font-size:16px;
        }
    </style>
</head>
```

**css and html class**
Classes allow you to use the same CSS styles on multiple HTML elements.
```
<style>
    .blue-text{
        color: blue;
    }
</style>

<h2 class="blue-text">Text</h2>

```
**css id attributes**

id attributes is that, like classes, you can style them using CSS.

However, an id is not reusable and should only be applied to one element. An id also has a higher specificity (importance) than a class so if both are applied to the same element and have conflicting styles, the styles of the id will be applied.

```
<style>
#cat-photo-element {
  background-color: green;
}
</style>

 <form action="/submit-cat-photo" id="cat-photo-form">
    <label><input type="radio" name="indoor-outdoor" checked> Indoor</label>
    <label><input type="radio" name="indoor-outdoor"> Outdoor</label><br>
    <label><input type="checkbox" name="personality" checked> Loving</label>
    <label><input type="checkbox" name="personality"> Lazy</label>
    <label><input type="checkbox" name="personality"> Energetic</label><br>
    <input type="text" placeholder="cat photo URL" required>
    <button type="submit">Submit</button>
  </form>
```

**css elements collection**

padding: 10px 20px 10px 20px;

margin: 10px 20px 10px 20px;

These four values work like a clock: top, right, bottom, left, 

10 px
1.5em

```
html tag | class {
    font-family:sans-serif;
    font-family: Helvetica, sans-serif;
    width: 500px;
    margin: px;
    padding: px;
    margin-top|left|right|bottom: px;
    padding-top|left|right|bottom: px;
}
```

**css background**
```
{
    background-color:green;
}

body {
    background-color:black;
}

```

**css border**

```
.thin-red-border {
    border-color:red;
    border-width:5px;
    border-style:solid;
    border-radius:10px;
    border-radius:50%;
}


<img class="class1 class2">
```

**css import font**

font-family: FAMILY_NAME, GENERIC_NAME;

```
<head>
    <link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">
    <style>
        font-family: FAMILY_NAME, GENERIC_NAME;
    </style>
</head>
```

**css use attribute selectors to style elements**

below code changes the margins of all elements with the attribute type and a corresponding value of radio

[attr=value] attribute selector to style 

```
<style>
[type='radio'] {
  margin: 20px 0px 20px 0px;
}
</style>
```

**Overrides All**

!important

```
<style>
  body {
    background-color: black;
    font-family: monospace;
    color: green;
  }
  #orange-text {
    color: orange;
  }
  .pink-text {
    color: pink !important;
  }
  .blue-text {
    color: blue;
  }
</style>
<h1 id="orange-text" class="pink-text blue-text" style="color: white">Hello World!</h1>
```

**css color**

* hex codes use 6 hexadecimal digits to represent colors, two each for red (R), green (G), and blue (B) components.

* The digit 0 is the lowest number in hex code, and represents a complete absence of color.

* The digit F is the highest number in hex code, and represents the maximum possible brightness.

* The RGB value for black looks like this:
```
rgb(0, 0, 0)
```

* The RGB value for white looks like this:
```
rgb(255, 255, 255)
```


```
body {
  color: #000000;
}

body {
  background-color: rgb(255, 165, 0);
}
```

**custom CSS Variable**

* give it a name with two hyphens in front of it and assign it a value like this:

```
--penguin-skin: gray;
```

*  assign its value to other CSS properties by referencing the name you gave it.

```
<style>
    h1 {
        background: var(--penguin-skin);
    }
</style>
```

* Fallback value to a CSS Variable, attach a fallback value that your browser will revert to if the given variable is invalid. This fallback is not used to increase browser compatibility, and it will not work on IE browsers. Rather, it is used so that the browser has a color to display if it cannot find your variable.

```
<style>
    h1 {
        background: var(--penguin-skin,black);
    }
</style>
```

**inherit css variable**

* To make use of inheritance, CSS variables are often defined in the :root element.

:root is a pseudo-class selector that matches the root element of the document, usually the html element. By creating your variables in :root, they will be available globally and can be accessed from any other selector in the style sheet.

When you create your variables in :root they will set the value of that variable for the whole page.

You can then over-write these variables by setting them again within a specific element.



```
<style>
  :root {
    --penguin-skin: gray;
    --penguin-belly: pink;
    --penguin-beak: orange;
  }

  body {
    background: var(--penguin-belly, #c6faf1);
  }

  .penguin {
    /* override inheritance */
    --penguin-belly:white;

</style>
```

**media query to change a variable**

when your screen is smaller or larger than your media query break point, you can change the value of a variable, and it will apply its style wherever it is used.

```
<style>
  :root {
    --penguin-size: 300px;
    --penguin-skin: gray;
    --penguin-belly: white;
    --penguin-beak: orange;
  }

  @media (max-width: 350px) {
    :root {
      /* Only change code below this line */
    --penguin-size:200px;
    --penguin-skin:black;
      /* Only change code above this line */
    }
  }
</style>
```