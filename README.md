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

These four values work like a clock: top, right, bottom, left, 

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

