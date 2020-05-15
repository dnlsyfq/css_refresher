# CSS 

## Linking css 
```
<link href="https://www.codecademy.com/stylesheets/style.css" type="text/css" rel="stylesheet">
<link href="./style.css" type="text/css" rel="stylesheet">
```

## Inline styles
```
<p style="color: red;">I'm learning to code!</p>
<p style="color: red; font-size: 20px;">I'm learning to code!</p>
```

## Head
```
<head>
  <style>
    p {
        color: red;
        font-size:20px;
    }

  </style>
</head>
```

## Tag Name
CSS can select HTML elements by using an element’s tag name. A tag name is the word (or character) between HTML angle brackets.
```
# the tag for a paragraph element is <p>. The CSS syntax for selecting <p> elements is

p {

}
```

## class Name
HTML elements can have more than just a tag name; they can also have attributes. One common attribute is the class attribute. It’s also possible to select an element by its class attribute
```
<p class="brand">Sole Shoe Company</p>

.brand {

}
```

it’s possible to add more than one class name to an HTML element’s class attribute

```
.green {
  color: green;
}

.bold {
  font-weight: bold;
}

<h1 class="green bold"> ... </h1>
```
## ID Name
HTML element needs to be styled uniquely (no matter what classes are applied to the element), we can add an ID to the element. To select an id element, CSS prepends the id name with a hashtag (#).
```
<h1 id="large-title"> ... </h1>

 #large-title {

}
```

## Class and ID
```
  <h1 id="article-title" class="title uppercase">Top Vacation Spots</h1>

```
---
> While classes are meant to be used many times, an ID is meant to style only one element. As we’ll learn in the next exercise, IDs override the styles of tags and classes. Since IDs override class and tag styles, they should be used sparingly and only on elements that need to always appear the same.
---

### Specificity
Specificity is the order by which the browser decides which CSS styles will be displayed. A best practice in CSS is to style elements while using the lowest degree of specificity, so that if an element needs a new style, it is easy to override.

> IDs are the most specific selector in CSS, followed by classes, and finally, tags

```
<h1 class="headline">Breaking News</h1>

h1 {
  color: red;
}

.headline {
  color: firebrick;
}

In the example code above, the color of the heading would be set to firebrick, as the class selector is more specific than the tag selector. If an ID attribute (and selector) were added to the code above, the styles within the ID selector’s body would override all other styles for the heading. The only way to override an ID is to add another ID with additional styling.
```

### Chaining Selectors
it’s possible to require an HTML element to have two or more CSS selectors at the same time.
This is done by combining multiple selectors, which we will refer to as chaining. For instance, if there was a .special class for h1 elements
```
h1.special {

}

# The code above would select only the h1 elements that have a class of special. If a p element also had a class of special, the rule in the example would not style the paragraph.
```

### Nested Elements
CSS also supports selecting elements that are nested within other HTML elements. 

```
<ul class='main-list'>
  <li> ... </li>
  <li> ... </li>
  <li> ... </li>
</ul>

.main-list li {

}
```
.main-list selects the .main-list element (the unordered list element). The nested <li> are selected by adding li to the selector, separated by a space, resulting in .main-list li as the final selector (note the space in the selector).




* font
```
font-family: Arial | cursive;
text-transform:capitalize;
```
