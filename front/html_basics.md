# INTRODUCTION TO HTML


HTML is a **front language**. It means what is displayed and visible on a web page as `images`, `videos` or `text content`.

This is the **skeleton** of all web pages, it provides the structure to the content appearing on a website.


## HTML skeleton


You can't writre as an anarchist. You have to **respect** some rules to display your content on browsers.

You have to think with **the following relation** :

- parent (``<html>``) `has many` children (``<head>``, ``<body>`` . . .)
- child (``<head>`` or ``<body>``) `belongs to one` parent (``<html>``)
- the `siblings` of ``<head>`` is ``<body>``


```html
<!-- beginning of file -->
<!DOCTYPE html>
<html>
    <head>
<!-- Page's intelligence = meta tags, external library or framework -->
</head>
<body>
<!-- Page's content = displayed on the page -->
    </body>
</html>
<!-- end of file -->
```

## Basic synthax


HTML is based on 3 different tags :

- `<element>` _[your content here]_ `</element>` --> the **opening** and **closing** tag
- _[your content here]_ `<element>` --> the **self opening** tag
- `<element/>` --> the **self closing** tag


#### 1. Examples of `opening` and `closing` tag


##### headers


```html
<h1>Title of the page</h1> <!-- Only one per page! SEO important -->
<h2>[...]</h2>
<h3>[...]</h3>
<h4>[...]</h4>
<h5>[...]</h5>
<h6>[...]</h6>
```

##### paragraphs


```html
<p>
Lorem ipsum dolor sit amet, consectetur adipisicing elit.
Veritatis laboriosam mollitia autem at ab omnis iure quis
asperiores inventore eos nam aut iusto officiis deserunt
nihil, sequi tempore impedit quae?
</p>
```

#### lists


HTML provides two king of list :

* `<ul>`the unordered lists
* `<ol>`the ordered lists


```html
<ul>
  <li>Ubisoft</li>                  <!-- ● Ubisoft -->
  <li>Activision</li>               <!-- ● Activision -->
  <li>EA</li>                       <!-- ● EA -->
</ul>
<h2>Ordered list</h2>
<ol>
  <li>Ubisoft</li>                  <!-- 1. Ubisoft -->
  <li>Activision</li>               <!-- 2. Activision -->
  <li>EA</li>                       <!-- 3. EA -->
</ol>
```

##### divs


`<div>` are **container** which can contain many other siblings tag element.


```html
<div>
    <h1>[...]</h1>
    <p>[...]<P>
</div>
```

#### 2. Example of `self opening` tag


##### images


```html
<img src="ubisoft_logo.png" alt="Ubisoft logo">
```

##### links


```html
<a href="https://www.ubisoft.com/fr-fr/">
```

#### 3. Example of `self closing` tag


##### inputs


```html
<input type="text" name="first_name"/>
<!-- useful in form -->
<form>
  <input type="text" name="email"/>
  <input type="text" name="password"/>
  <button type="submit">sign in</button>
</form>
```

### Much more (RTFM)

⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️

**R**ead **T**he **F**ucking **M**anual is an expression that can not be spoken out loud, but cannot be repeated often enough. Probably 80% of the problems programers experience with their code can be resolved by RTFM

⚠️⚠️⚠️⚠️⚠️⚠️⚠️⚠️


[codeguide.co](https://codeguide.co/)

[MDN Reference](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)

#### 4. Special tags


**Some html tags allow us to target a specific piece of content.** We call them `Emphasizing` tag.

`<em>` puts the content in italic style and `<strong>`puts it in bold :


```html
<p>
You can emphasize <em>some words</em>, <!-- italic --> and even <strong>more if needed</strong> <!-- bold -->
</p>
```

## Attributes


**Attributes are element that apply specific style on a html content**.

The attributes are useful when you `write CSS code`.

For example, you can apply a specific `color` or `font-size` to the content between the attribute than the rest of the content :


```html
<p>
You can add an attribute to span <span class="something">and add some different
stylesheet</span> than the rest of the text. </p>
<!-- here <span> is an emphazing tag like <em> or <strong> but with a neutral behavior. The attribute 'class' overwritte his default behavior by adding the style you want -->
```

HTML provides two different attributes :

- `id`
- `class`

These two attributes **run the same job with one difference** : **`id` can identify only ONE element** and **`class` can identify MORE than one.**

# HAPPY HACKING !!

