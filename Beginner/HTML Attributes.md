# HTML Attributes

- All Html element can have attributes
- Attributes provide additional information about elements
- Attributes are always specified in the start tag.
- Attributes usually come in name/value paris like `name="value"`

```html
<a href="https://www.w3schools.com">Visit W3Schools</a>
```
```html
<img src="img_girl.jpg">
```
```html
<img src="img_girl.jpg" width="500" height="600">
```
```html
<p style="color:red;">This is a red paragraph.</p>
```
```html
<html lang="en">
```


## Global Attributes
### 1️⃣ accesskey
```html
<a href="https://www.w3schools.com/html/" accesskey="h">HTML</a><br>
```
> [!CAUTION]
> Using accesskey is dificult because they may conflict with other key standards in the browser. To avoid this problem , most browser will use accesskey only if pressed together with the Alt key.

### 2️⃣ class
```html
<html>
<head>
<style>
    h1.intro {
    color: blue;
    }

    p.important {
    color: green;
    }
</style>
</head>
<body>
    <h1 class="intro">Header 1</h1>
    <p>A paragraph.</p>
    <p class="important">Note that this is an important paragraph.</p>
</body>
</html>
```
```js
document.getElementById("myDIV").classList.add("mystyle");
```

### 3️⃣ contenteditable
```html
<p contenteditable="true">This is an editable paragraph.</p>
```

 ### data-*
 > [!NOTE]
 > The `data-*` attributes in HTML are custom attributes used to store extra information (metadata) that isn't visible to users but can accessed using JavaScript.
 ```html
 <ul>
  <li data-animal-type="bird">Owl</li>
  <li data-animal-type="fish">Salmon</li>
  <li data-animal-type="spider">Tarantula</li>
</ul>
 ```
```html
<button data-tooltip="Click me!">Hover Me</button>

<script>
  let button = document.querySelector("button");
  button.addEventListener("mouseover", function () {
    alert(button.dataset.tooltip); // Shows "Click me!"
  });
</script>
```

### 4️⃣ dir
```html
<p dir="rtl">Write this text right-to-left!</p>
```
- ltr
- rtl 
- auto // only use when direction unknown

### 5️⃣ draggable
```html
<p draggable="true">This is a draggable paragraph.</p>
```

### 6️⃣ enterkeyhint
```html
<input type="text" enterkeyhint="done">
<input type="text" enterkeyhint="enter">
<input type="text" enterkeyhint="next">
<input type="text" enterkeyhint="previous">
<input type="text" enterkeyhint="search">
<input type="text" enterkeyhint="go">
<input type="text" enterkeyhint="send">
```

### 7️⃣ hidden
```html
<p hidden>This paragraph should be hidden.</p>
```
```html
<p id="text" hidden>This paragraph should be hidden.</p>
<button onclick="showText()">Show</button>

<script>
  function showText() {
    document.getElementById("text").hidden = false;
  }
</script>
```

### 8️⃣ id
> [!NOTE]
> same as `class` but it must be uniuqe in html document.
```html
<h1 id="myHeader">Hello World!</h1>
```

#### bookmark in page
```html
<h2><a id="top">Some heading</a></h2>

<p>Lots of text....</p>
<p>Lots of text....</p>
<p>Lots of text....</p>

<a href="#top">Go to top</a>
```

### 9️⃣ inert
> [!NOTE]
> The `inert` attribute disables an element and all the elements inside.
```html
<div inert>
  <button onclick="alert(42)">
  <input type="text">
  <a href="https://w3schools.com">W3Schools.com</a>
</div>
```

### 1️⃣0️⃣ inputmode
```html
<input type="text" inputmode="numeric">
<input type="text" inputmode="decimal">
<input type="text" inputmode="email">
<input type="text" inputmode="none">
<input type="text" inputmode="search">
<input type="text" inputmode="tel">
<input type="text" inputmode="text">
<input type="text" inputmode="url">
```

### 1️⃣1️⃣ lang
```html
<p lang="fr">Ceci est un paragraphe.</p>
```

### 1️⃣1️⃣  popover
```html
<h1 popover id="myheader">Hello</h1>
<button popovertarget="myheader">Click me!</button>
```

### 1️⃣2️⃣ spellcheck
```html
<p contenteditable="true" spellcheck="true">This is a paragraph.</p>
```

### 1️⃣3️⃣ style
```html
<h1 style="color:blue;text-align:center;">This is a header</h1>
<p style="color:green;">This is a paragraph.</p>
``` 

### 1️⃣4️⃣ tabindex
```html
<a href="https://www.w3schools.com/" tabindex="2">W3Schools</a>
<a href="http://www.google.com/" tabindex="1">Google</a>
<a href="http://www.microsoft.com/" tabindex="3">Microsoft</a>
```

### 1️⃣5️⃣ title
```html
<p><abbr title="World Health Organization">WHO</abbr> was founded in 1948.</p>
<p title="Free Web tutorials">W3Schools.com</p>
``` 

### 1️⃣6️⃣ translate
```html
<p translate="no">Don't translate this!</p>
<p>This can be translated to any language.</p>
```