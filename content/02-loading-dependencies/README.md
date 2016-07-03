# Loading Dependencies

Now lets add a new file that we will use as a dependencie of our main JS.

**content.js**
```js
module.exports = "It works from content.js.";
```

And change **entry,js** file:
```js
document.write(require("./content.js"));
```

Lets recompile our bundle:
```bash
$ webpack ./entry.js bundle.js
```

Update your browser window and you should see the text `It works from content.js.`.
