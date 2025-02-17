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

**Img**
```
<img src="" alt="">
```

### CSS Grid

```



```

# HTML5

HTML5 introduced a number of new elements that give developers more options while also incorporating accessibility features. These tags include main, header, footer, nav, article, and section

**Note about section and div**

The section element is also new with HTML5, and has a slightly different semantic meaning than article. An article is for standalone content, and a section is for grouping thematically related content. They can be used within each other, as needed. For example, if a book is the article, then each chapter is a section. When there's no relationship between groups of content, then use a div.

```
<div> - groups content
<section> - groups related content
<article> - groups independent, self-contained content

```

**Note about head and header**

Note: The header is meant for use in the body tag of your HTML document. This is different than the head element, which contains the page's title, meta information, etc.

**Navigation**

nav element is another HTML5 item with the embedded landmark feature for easy screen reader navigation. This tag is meant to wrap around the main navigation links in your page

```
<body>
  <header>
    <h1>Training with Camper Cat</h1>

    <nav>
      <ul>
        <li><a href="#stealth">Stealth &amp; Agility</a></li>
        <li><a href="#combat">Combat</a></li>
        <li><a href="#weapons">Weapons</a></li>
      </ul>
    </nav>

  </header>
  <main>
    <section id="stealth">
      <h2>Stealth &amp; Agility Training</h2>
      <article><h3>Climb foliage quickly using a minimum spanning tree approach</h3></article>
      <article><h3>No training is NP-complete without parkour</h3></article>
    </section>
    <section id="combat">
      <h2>Combat Training</h2>
      <article><h3>Dispatch multiple enemies with multithreaded tactics</h3></article>
      <article><h3>Goodbye world: 5 proven ways to knock out an opponent</h3></article>
    </section>
    <section id="weapons">
      <h2>Weapons Training</h2>
      <article><h3>Swords: the best tool to literally divide and conquer</h3></article>
      <article><h3>Breadth-first or depth-first in multi-weapon training?</h3></article>
    </section>
  </main>
</body>

```


**Audio**

audio element gives semantic meaning when it wraps sound or audio stream content in your markup. Audio content also needs a text alternative to be accessible to people who are deaf or hard of hearing. This can be done with nearby text on the page or a link to a transcript.

The audio tag supports the controls attribute. This shows the browser default play, pause, and other controls, and supports keyboard functionality. This is a boolean attribute, meaning it doesn't need a value, its presence on the tag turns the setting on.

```
<audio id="meowClip" controls>
  <source src="audio/meow.mp3" type="audio/mpeg" />
  <source src="audio/meow.ogg" type="audio/ogg" />
</audio>
```
**Figure**

the figure element, along with the related figcaption. Used together, these items wrap a visual representation (like an image, diagram, or chart) along with its caption. 

```
<figure>
  <img src="roundhouseDestruction.jpeg" alt="Photo of Camper Cat executing a roundhouse kick">
  <br>
  <figcaption>
    Master Camper Cat demonstrates proper form of a roundhouse kick.
  </figcaption>
</figure>
```

```
<body>
  <header>
    <h1>Training</h1>
    <nav>
      <ul>
        <li><a href="#stealth">Stealth &amp; Agility</a></li>
        <li><a href="#combat">Combat</a></li>
        <li><a href="#weapons">Weapons</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <section>

      <!-- Only change code below this line -->
      <figure>
        <!-- Stacked bar chart will go here -->
        <br>
        <figcaption>Breakdown per week of time to spend training in stealth, combat, and weapons.</figcaption>
      </figure>
      <!-- Only change code above this line -->

    </section>
    <section id="stealth">
      <h2>Stealth &amp; Agility Training</h2>
      <article><h3>Climb foliage quickly using a minimum spanning tree approach</h3></article>
      <article><h3>No training is NP-complete without parkour</h3></article>
    </section>
    <section id="combat">
      <h2>Combat Training</h2>
      <article><h3>Dispatch multiple enemies with multithreaded tactics</h3></article>
      <article><h3>Goodbye world: 5 proven ways to knock out an opponent</h3></article>
    </section>
    <section id="weapons">
      <h2>Weapons Training</h2>
      <article><h3>Swords: the best tool to literally divide and conquer</h3></article>
      <article><h3>Breadth-first or depth-first in multi-weapon training?</h3></article>
    </section>
  </main>
  <footer>&copy; 2018 Camper Cat</footer>
</body>

```

**Form Label**

label tag wraps the text for a specific form control item, usually the name or label for a choice. This ties meaning to the item and makes the form more readable. The for attribute on a label tag explicitly associates that label with the form control and is used by screen readers.

```
<form>
  <label for="name">Name:</label>
  <input type="text" id="name" name="name">
</form>
```

```
<form>
  <fieldset>
    <legend>Choose one of these three items:</legend>
    <input id="one" type="radio" name="items" value="one">
    <label for="one">Choice One</label><br>
    <input id="two" type="radio" name="items" value="two">
    <label for="two">Choice Two</label><br>
    <input id="three" type="radio" name="items" value="three">
    <label for="three">Choice Three</label>
  </fieldset>
</form>
```

**Date, Time**

HTML5 introduced an option to specify a date field. Depending on browser support, a date picker shows up in the input field when it's in focus, which makes filling in a form easier for all users.

For older browsers, the type will default to text, so it helps to show users the expected date format in the label or as placeholder text just in case.

```
<label for="input1">Enter a date:</label>
<input type="date" id="input1" name="input1">
```

```
<p> Buy a monitor 
<time datetime="2013-02-13"> last Wednesday </time> for less expensive

<time datetime="2013-02-32"> <t>indepence </t></time>
</p>

```

# CSS Selectors
### ID
```
<p id="content"></p>

#content {
  font-size:27px;
}
```
### Class
```
<div class="title"></div>

.title{
  font-size:54px;
}
```
### Type
```
<button> Go to </button>

button {
  background-color:purple;
  height: 150px;
  color: white;
  widthL 300px;
}
```
### pseudo-class
```
selector:pseudo-class {
  property: value;
}

selector:hover {
  property: value;
}

```

### attributes
```
Attributes
Attribute selectors are a special kind of selector that will match elements based on their attributes and attribute values.

Their generic syntax consists of square brackets ([]) containing an attribute name followed by an optional condition to match against the value of the attribute.

Attribute selectors can be divided into two categories depending on the way they match attribute values:

Presence and value attribute selectors and
Substring value attribute selectors.
These attribute selectors try to match an exact attribute value:

[attr] This selector will select all elements with the attribute attr, whatever its value.
[attr=val] This selector will select all elements with the attribute attr, but only if its value is val.
[attr~=val] This selector will select all elements with the attribute attr, but only if val is one of a space-separated list of words contained in attr's value. (This one is a bit more complex, so checking some documentation might be helpful.)

img[alt]{
  
}
```

```
h1,
h2,
h3,
h4,
h5,
h6 {
  font-family: "Helvetica", "Arial", sans-serif;
}
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
    background-color:#dddddd;
    background-color:#ddd;
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

**CSS Reader**

visually hide content meant for screen readers (sr)

```
.sr-only{
  position:absolute;
  left:-10000px;
  width:1px;
  height:1px;
  top:auto;
  overflow:hidden;
}

<!-- except for  -->
<!-- hides content for everyone  -->
  {
    display:none;
    visibility:hidden
  }

<!-- remove from flow  -->
  {
    width: 0px;
    height: 0px;
  }





```

**Color Contrast**

Recommended contrast ratio 4.5:1 

hsl(0,%,%)
hsl(120,25%,%%)


**Button keyboard shortcut**

<button accesskey="b">Important</button>

**Tab keyboard focus**

tabindex attr has 3 distinct function  relate to keyboard focus. When its on tag it can be focused on 

div, span ,p can use tabindex="0" attr . tabindex="-1" , element is focusable but not reachable by keyboard


```
<div tabindex="0>I need focus</div>

```

```
<head>
  <style>
  p:focus {
    background-color: yellow;
  }
  </style>
</head>
<body>
  <header>
    <h1>Ninja Survey</h1>
  </header>
  <section>
    <form>


      <p tabindex="0">Instructions: Fill in ALL your information then click <b>Submit</b></p>


      <label for="username">Username:</label>
      <input type="text" id="username" name="username"><br>
      <fieldset>
        <legend>What level ninja are you?</legend>
        <input id="newbie" type="radio" name="levels" value="newbie">
        <label for="newbie">Newbie Kitten</label><br>
        <input id="intermediate" type="radio" name="levels" value="intermediate">
        <label for="intermediate">Developing Student</label><br>
        <input id="master" type="radio" name="levels" value="master">
        <label for="master">9th Life Master</label>
      </fieldset>
      <br>
      <fieldset>
      <legend>Select your favorite weapons:</legend>
      <input id="stars" type="checkbox" name="weapons" value="stars">
      <label for="stars">Throwing Stars</label><br>
      <input id="nunchucks" type="checkbox" name="weapons" value="nunchucks">
      <label for="nunchucks">Nunchucks</label><br>
      <input id="sai" type="checkbox" name="weapons" value="sai">
      <label for="sai">Sai Set</label><br>
      <input id="sword" type="checkbox" name="weapons" value="sword">
      <label for="sword">Sword</label>
      </fieldset>
      <br>
      <input type="submit" name="submit" value="Submit">
    </form><br>
  </section>
  <footer>&copy; 2018 Camper Cat</footer>
</body>

```
