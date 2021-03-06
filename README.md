# LoDashed
[![Build Status](http://img.shields.io/travis/gustavohenke/lodashed.svg?style=flat-square)](https://travis-ci.org/gustavohenke/lodashed) [![Dependency Status](http://img.shields.io/david/dev/gustavohenke/lodashed.svg?style=flat-square)](https://gemnasium.com/gustavohenke/lodashed)
[![NPM version](http://img.shields.io/npm/v/lodashed.svg?style=flat-square)](http://badge.fury.io/js/lodashed)

Lo-Dash, Underscore.string + some other useful functions in a single, powerful `_`.

## The "other" functions

#### `.type( [variable] )`
Return the type of a variable as a string.

```javascript
_.type([]); // => array
_.type(new Array()); // => array
_.type({}); // => object
_.type(new Object()); // => object
```

#### `.uncapitalize( [str] )`
Uncapitalize an string.

```javascript
_.uncapitalize( "I AM MAD!" ); // "i AM MAD!"
_.uncapitalize( "you're my hero!" ); // "you're my hero!"
```

#### `.replaceAll( str, token, newToken[, ignoreCase])`
Replace all occurrences of an string, optionally checking the case.

```javascript
_.replaceAll( "Anakin Skywalker was the best jedi!", "Anakin", "Luke" ); // => Luke Skywal...
_.replaceAll( "Anakin Skywalker was the best jedi!", "anakin", "Luke" ); // => Anakin Skywal...
_.replaceAll( "Anakin Skywalker was the best jedi!", "anakin", "Luke", true ); // => Luke Skywal...
```

#### `.uuid()`
Returns an UUID v4.

```javascript
_.uuid(); // => "9279f99f-0525-4079-95a6-3580ef272e71"
```

#### `.byteFormat( bytes[, decimals=0][, decimalSeparator="."][, orderSeparator=","] )`
Format an byte size, e.g. 1024 becomes 1 KB. You can also customize the output by providing how much `decimals` you want and a `decimalSeparator` and `orderSeparator`.

```javascript
_.byteFormat( 1024 ); // => "1 KB"
_.byteFormat( 1024 * 100 ); // => "100 KB"
```

## Tests
Run the following commands inside the project root:

```shell
npm install
npm test
```

## License
MIT
