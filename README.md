# LoDashed [![Build Status](https://travis-ci.org/gustavohenke/lodashed.png)](https://travis-ci.org/gustavohenke/lodashed)

Lo-Dash, Underscore.string + some other useful functions in a powerful _.

## The "other" functions

### `.type( [variable] )`
Return the type of a variable as a string.

```javascript
_.type([]); // => array
_.type(new Array()); // => array
_.type({}); // => object
_.type(new Object()); // => object
```

### `.uncapitalize( [str] )`
Uncapitalize an string.

```javascript
_.uncapitalize( "I AM MAD!" ); // "i AM MAD!"
_.uncapitalize( "you're my hero!" ); // "you're my hero!"
```

### `.extendDeep( [object] )` _alias:_ assignDeep
Deep version of the `_.extend()` function.

```javascript
_.extendDeep({ a: { b: true } }, { a: { c: 123 } }); // => { a: { b: true, c: 123 } }
```

### `.replaceAll( str, token, newToken[, ignoreCase])`
Replace all occurrences of an string, optionally checking the case.

```javascript
_.replaceAll( "Anakin Skywalker was the best jedi!", "Anakin", "Luke" ); // => Luke Skywal...
_.replaceAll( "Anakin Skywalker was the best jedi!", "anakin", "Luke" ); // => Anakin Skywal...
_.replaceAll( "Anakin Skywalker was the best jedi!", "anakin", "Luke", true ); // => Luke Skywal...
```

### `.uuid()`
Returns an UUID v4.

```javascript
_.uuid(); // => "9279f99f-0525-4079-95a6-3580ef272e71"
```

### `.byteFormat( bytes[, decimals][, decimalSeparator][, orderSeparator] )`
Format an byte size, e.g. 1024 becomes 1 KB.

```javascript
_.byteFormat( 1024 ); // => "1 KB"
_.byteFormat( 1024 * 100 ); // => "100 KB"
```