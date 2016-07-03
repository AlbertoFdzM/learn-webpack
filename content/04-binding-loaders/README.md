# Binding loaders

We don’t want to write such long requires `require('!style!css!./style.css');`.

We can bind file extensions to loaders so we just need to write: `require(''./style.css')``

Update **entry.js**
```js
require('./style.css');
document.write(require('./content.js'));
```

Run the compilation with:
```bash
webpack ./entry.js bundle.js --module-bind 'css=style!css'
```
Some environments may require double quotes: `–module-bind "css=style!css"`

You should see the same result.
