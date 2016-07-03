# First Steps

Start with a empty directory.

Create these files:

**entry.js**
```js
document.write("It works.");
```

**index.html**
```html
<html>
    <head>
        <meta charset="utf-8">
    </head>
    <body>
        <script type="text/javascript" src="bundle.js" charset="utf-8"></script>
    </body>
</html>
```

Then run the following command:
```bash
$ webpack ./entry.js bundle.js
```

It will compile your file and create a bundle file.

If successful it displays something like this:
```bash
Version: webpack 1.12.11
Time: 51ms
    Asset     Size  Chunks             Chunk Names
bundle.js  1.42 kB       0  [emitted]  main
chunk    {0} bundle.js (main) 28 bytes [rendered]
    [0] ./tutorials/getting-started/setup-compilation/entry.js 28 bytes {0} [built]
```

Open index.html in your browser.

It should display `It works`.
