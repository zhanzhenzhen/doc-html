# doc-html

Two features:

- prettify `<pre>`
- switch between multiple human languages, or multiple programming languages

If you are writing a manual/documentation of your project but find Markdown is too simple and HTML is too complicated/ugly, you have come to the right place!

Put this before all other script elements:

```html
<script src="doc-html.js" type="text/javascript"></script>
```

It's fully browser-side. Don't use it for any server-side purposes.

# `<pre>` indentation

It will detect indentation in `<pre>` elements and display them correctly.

```html
<body>
    <pre><code>
        var a = function() {
            alert("something");
        };
    </code></pre>
</body>
```

After applying doc-html, the first 8 white spaces in each line will be removed.

# Multiple languages

If you want your page to be able to seamlessly switch between English and Chinese, and between JavaScript and CoffeeScript, then you can write:

```javascript
var naturalLangs = ["en", "zh"];
var programLangs = ["js", "coffee"];
```

then in a button callback:

```javascript
setLang("zh", naturalLangs);
```

in another button callback:

```javascript
setLang("coffee", programLangs);
```

All elements with these 4 class names will be toggled.

# Real page example

It's used by my "wishlist" tutorial:

[Click to see](http://zhanzhenzhen.github.io/wishlist/) (this HTML page is fully hand-written).
