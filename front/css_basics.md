# INTRODUCTION TO CSS (Cascading Style Sheets)

CSS is a language used on web page to formated and stylized HTML files.

## ❤️ Rules ❤️

#### Linking stylesheet to HTML page


```html
<!-- index.html -->
[...]
<head>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Hello Ubisoft</h1>
</body>
```

```css
/* style.css */
h1 {
  color: red;
  font-weight: bold;
}
```

#### CSS syntax

- **selector** means a selection of one or more elements of the page.
- **property** on which we call the style property.
- **value** on which we define style rules.


```css
/* style.css */
selector {
  property: value;
  property: value;
  property: value;
}
```

## 🚀 Examples 🚀


- `h1` equals to **selector**.
- `color`, `font-size`, and `font-weight`  are equal to **property**.
- `red`, `20px`, and `bold`  are equal to **value**.


```css
/* style.css */
h1 {
  color: red;
  font-size: 20px;
  font-weight: bold;
}
```

#### Tag name

makes **all** `h1` elements **red** and **bold**.


```html
<!-- index.html -->
[...]
<body>
  <h1>Hello World</h1>
</body>
```

combined with

```css
/* style.css */
h1 {
  color: red;
  font-weight: bold;
}
```

#### Class name

will make only the **second** and **third** paragraphs **justified**.


```html
<!-- index.html -->
[...]
<body>
  <p>This paragraph is not justified</p>
  <p class="text-justify">This one is</p>
  <p class="text-justify">This one also</p>
</body>
```

combined with

```css
/* style.css */
.text-justify {
  text-align: justify;
}
```

#### Multiple classes

will make the **paragraph** `<p>` **justified** and **red**.


```html
<!-- index.html -->
[...]
<body>
  <p class="text-justify text-red">This one is</p>
</body>
```

combined with

```css
/* style.css */
.text-justify {
  text-align: justify;
}
.text-red {
  color: red;
}
```

#### ID name

will put an image background on the **unique** div with `id="banner"`.


```html
<!-- index.html -->
<body>
  <div id="banner">
    <h1>Ubisoft</h1>
    <p>We bring video games to people</p>
  </div>
</body>
```

combined with

```css
/* style.css */
#banner {
  background-image: url("example.jpg");
  background-size: cover;
}
```

#### Specificity

will make the header `<h1>` **yellow** because `.main-title`class selector is more specific than the tag selector.

```html
<h1 class="main-title">Ubisoft</h1>
```

combined with

```css
h1 {
  color: red;
}
.main-title {
  color: yellow;
}
```

#### ⚠️ Important! ⚠️

⚠️will make the header `<h1>` **red** because `important!` **overwrite** `.main-title`class selector. ⚠️


```html
<h1 class="main-title">Ubisoft</h1>
```

combined with

```css
h1 {
  color: red important!;
}
.main-title {
  color: yellow;
}
```

#### Nested Elements

`h1` **children** of the element `id="banner"` will be **white**.


```html
<!-- index.html -->
<body>
  <div id="banner">
    <h1>Ubisoft</h1>
    <p>We bring video games to people</p>
  </div>
</body>
```

combined with

```css
/* style.css */
#banner h1 {
  color: white;
}
```

#### Direct Children

`a` **direct children** of `li` **direct children** of `id="navigation"` will be **blue**.


```html
<!-- index.html -->
<body>
  <ul id="navigation">
    <li><a href="#">Home</a></li>
    <li><a href="#">Team</a></li>
    <li><a href="#">Contact</a></li>
  </ul>
</body>
```

combined with

```css
/* style.css */
#navigation > li > a {
  color: blue;
}
```

#### Grouping


```css
/* style.css */
h1, h2, h3 {
  font-weight: bold;
}
```

is a shortcut syntax for

```css
/* style.css */
h1 {
  font-weight: bold;
}
h2 {
  font-weight: bold;
}
[...]
```

#### Pseudo Classes

will make links underlined **when the mouse hovers** over them.


```css
/* style.css */
a {
  color: red;
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
}
```

⚠️ **R**ead **T**he **F**ucking **M**anual is an expression that can not be spoken out loud, but cannot be repeated often enough. Probably 80% of the problems programers experience with their code can be resolved by RTFM ⚠️

👉 See [other pseudo classes.](https://developer.mozilla.org/en/docs/Web/CSS/Pseudo-classes)


## 💡 Tips 💡

#### Colors - Tips

- **RGB** stands for **R**ed **G**reen **B**lue
- each value is between **0** and **255**
- for same values of R, G and B, you are on the grey scale


```css
body {
  color: rgb(10, 10, 10);
}
```

#### Colors


```css
color: #FF530D;
color: rgb(255, 83, 13);
color: rgba(255, 83, 13, 1.0);
```

#### Box Model

![box_model](./assets/box_model.png)

#### Box Model - Border

#### Borders


```css
div {
  border: 1px solid red;
}
/* or */
div {
  border-top: 1px solid red;
  border-right: 2px dotted black;
  border-bottom: 1px dashed green;
  border-left: 2px dotted black;
}
```

![Image associée](http://4.bp.blogspot.com/-Xw7CNA4MM6o/UIjUjzN-FQI/AAAAAAAABX0/xfnKFZuoiSU/s1600/border_style.jpg)

#### Border radius

![enter image description here](https://www.1keydata.com/css-tutorial/border-radius-illustration.png)

#### Units


```css
/* Absolute */
p {
  width: 50px;
}
/* Relative to parent */
p {
  width: 50%;
}
/* Relative to font size */
p {
  width: 2em;
}
```

## 🔨 Components 🔨

**How build structured components ?**


#### Flexbox components

**95% of components are coded with flexbox 💪**

#### Flexbox - vocabulary


```css
.container {
  display: flex;
}
.items {
  flex: 1;
}
```

![enter image description here](https://css-tricks.com/wp-content/uploads/2018/10/01-container.svg)

![enter image description here](https://css-tricks.com/wp-content/uploads/2018/10/02-items.svg)

#### Flexbox - justify content


```css
.container {
  display: flex;
  justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;
}
.items {
  flex: 1;
}
```

![enter image description here](https://css-tricks.com/wp-content/uploads/2018/10/justify-content.svg)

#### Flexbox - align items


```css
.container {
  display: flex;
  align-items: stretch | flex-start | flex-end | center | baseline;
}
```

![enter image description here](https://css-tricks.com/wp-content/uploads/2018/10/align-items.svg)

#### Flex item - flex grow


```css
.container {
  display: flex;
  align-items: center;
}
.item {
  flex-grow: <number>; /* 1 | 2 */
}
```

![enter image description here](https://css-tricks.com/wp-content/uploads/2018/10/flex-grow.svg)


## 🏋️‍♀️ Training 🏋️‍♀️


**Want improve your skills ?**


👉 [learn flexbox as a boss](https://flexboxfroggy.com/#fr)

⚠️ **R**ead **T**he **F**ucking **M**anual is an expression that can not be spoken out loud, but cannot be repeated often enough. Probably 80% of the problems programers experience with their code can be resolved by RTFM ⚠️

👉 [CSS guides](https://css-tricks.com/guides/)


# HAPPY HACKING !
