# to-integer

> Converts the given value to an integer. 


[![MIT License](https://img.shields.io/badge/license-MIT_License-green.svg?style=flat-square)](https://github.com/bubkoo/to-integer/blob/master/LICENSE)

[![build:?](https://img.shields.io/travis/bubkoo/to-integer/master.svg?style=flat-square)](https://travis-ci.org/bubkoo/to-integer)
[![coverage:?](https://img.shields.io/coveralls/bubkoo/to-integer/master.svg?style=flat-square)](https://coveralls.io/github/bubkoo/to-integer)


## Install

```
$ npm install --save to-integer 
```


## Usage

> For more use-cases see the [tests](https://github.com/bubkoo/to-integer/blob/master/test/spec/index.js)

```js
var toInteger = require('to-integer');

toInteger(1);                // => 1
toInteger();                 // => 0
toInteger(null);             // => 0
toInteger(Number.MAX_VALUE); // => Number.MAX_VALUE
toInteger(Infinity);         // => Infinity

// boolean
toInteger(true);  // => 1
toInteger(false); // => 0

// string
toInteger('1');      // => 1
toInteger('0');      // => 0
toInteger('-1');     // => -1
toInteger('1.1000'); // => 1
toInteger('-1.100'); // => -1
toInteger('01');     // => 1
toInteger('0.10');   // => 0
toInteger('1a');     // => 1
toInteger('a1');     // => NaN

// binary
toInteger('0b01'); // => 1
toInteger('0b10'); // => 2
toInteger('0b11'); // => 3
toInteger('0b02'); // => NaN

// octal
toInteger('0o01'); // => 1 
toInteger('0o07'); // => 7
toInteger('0o10'); // => 8
toInteger('0o08'); // => NaN

// hex
toInteger('0x01');  // => 1 
toInteger('0x0F');  // => 15 
toInteger('0x0G');  // => NaN
toInteger('-0x01'); // => NaN
toInteger('+0x01'); // => NaN

// object
toInteger(new Object(1));   // => 1
toInteger(new Number(1));   // => 1
toInteger(new Number(1.1)); // => 1
toInteger(function () {});  // => NaN 
toInteger(new Object());    // => NaN
```

## Related

- [to-num](https://github.com/bubkoo/to-num) - Converts the given value to a number.
- [to-length](https://github.com/bubkoo/to-length) - Converts value to an integer suitable for use as the length of an array-like object.
- [to-str](https://github.com/bubkoo/to-str) - Converts the given value to a string.
- [to-lower](https://github.com/bubkoo/to-lower) - Converts string, as a whole, to lower case.
- [to-upper](https://github.com/bubkoo/to-upper) - Converts string, as a whole, to upper case.
- [to-path](https://github.com/bubkoo/to-path) - Converts value to a property path array. 
- [to-source-code](https://github.com/bubkoo/to-source-code.git) - Converts function to its source code.
- [upper-first](https://github.com/bubkoo/upper-first) - Converts the first character of string to upper case.
- [lower-first](https://github.com/bubkoo/lower-first) - Converts the first character of string to lower case.


## Contributing

Pull requests and stars are highly welcome.

For bugs and feature requests, please [create an issue](https://github.com/bubkoo/to-integer/issues/new).
