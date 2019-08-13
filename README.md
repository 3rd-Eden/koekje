# koekje

Koekje is dutch for `cookie` and it's also DOM Storage API compatible storage
layer for storing data in a... **cookie**.

## Installation

This module was designed with browserify in mind and can be installed from the
public npm registry:

```
npm install --save koekje
```

## Usage

In all examples we assume that you've required the module as:

```js
'use strict';

var koekje = require('koekje');
```

The API is we expose is compatible with the API of the DOM Storage methods. They
can be found at:

https://developer.mozilla.org/en-US/docs/Web/API/Storage

```js
koekje.setItem('foo', 'bar');  // Returns undefined and stores the value.
koekje.getItem('bar');         // Not found, returns null.
koekje.getItem('foo');         // Returns `bar`.
koekje.length;                 // 1
koekje.removeItem('foo');      // Returns undefined, length is now 0.
koekje.clear();                // Returns undefined and clears all items.
```

## License

[MIT](LICENSE)
