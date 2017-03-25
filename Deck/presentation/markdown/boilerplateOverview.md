# Looking into our codebase

Let's look at our `index.html` file.

```html
<html>
<head>
    <title>Sample App</title>
    <link rel="shortcut icon" href="">
    <!-- A stylesheet for our application -->
    <link rel="stylesheet" href="https://unpkg.com/tachyons@4.6.1/css/tachyons.min.css"/>
</head>
<body>
    <div id='root'></div>
    <script src="/static/bundle.js"></script>
</body>
</html>
```

- Inside of the `<head/>` is where we can store metadata for the webpage (title, styles, favicon, etc).
    + The [Tachyons](http://tachyons.io/) stylesheet has been added for some style
- The script `bundle.js` is the react application once it's been compiled.
- The div with an id of `root` is where the react application mounts itself to.