# is-number [![NPM version](https://badge.fury.io/js/is-number.svg)](http://badge.fury.io/js/is-number)

> Returns true if the value is a number. comprehensive tests.

To understand some of the rationale behind the decisions made in this library (and to learn about some oddities of number evaluation in JavaScript), [see this gist][gist].


## Install with [npm](npmjs.org)

```bash
npm i is-number --save
```


## Usage

```js
var isNumber = require('is-number');
```

### true

See the [tests](./test.js) for more examples.

```js
isNumber(5e3)      //=> 'true'
isNumber(0xff)     //=> 'true'
isNumber(-1.1)     //=> 'true'
isNumber(0)        //=> 'true'
isNumber(1)        //=> 'true'
isNumber(1.1)      //=> 'true'
isNumber(10)       //=> 'true'
isNumber(10.10)    //=> 'true'
isNumber(100)      //=> 'true'
isNumber('-1.1')   //=> 'true'
isNumber('0')      //=> 'true'
isNumber('012')    //=> 'true'
isNumber('0xff')   //=> 'true'
isNumber('1')      //=> 'true'
isNumber('1.1')    //=> 'true'
isNumber('10')     //=> 'true'
isNumber('10.10')  //=> 'true'
isNumber('100')    //=> 'true'
isNumber('5e3')    //=> 'true'
isNumber(parseInt('012'))   //=> 'true'
isNumber(parseFloat('012')) //=> 'true'
```

### False

See the [tests](./test.js) for more examples.

```js
isNumber('foo')             //=> 'false'
isNumber([1])               //=> 'false'
isNumber([])                //=> 'false'
isNumber(function () {})    //=> 'false'
isNumber(Infinity)          //=> 'false'
isNumber(NaN)               //=> 'false'
isNumber(new Array('abc'))  //=> 'false'
isNumber(new Array(2))      //=> 'false'
isNumber(new Buffer('abc')) //=> 'false'
isNumber(null)              //=> 'false'
isNumber(undefined)         //=> 'false'
isNumber({abc: 'abc'})      //=> 'false'
```

## Run tests

Install dev dependencies:

```bash
npm i -d && npm test
```

## Author

**Jon Schlinkert**
 
+ [github/jonschlinkert](https://github.com/jonschlinkert)
+ [twitter/jonschlinkert](http://twitter.com/jonschlinkert) 

## License
Copyright (c) 2015 Jon Schlinkert  
Released under the MIT license

***

_This file was generated by [verb](https://github.com/assemble/verb) on January 24, 2015._

[infinity]: http://en.wikipedia.org/wiki/Infinity
[gist]: https://gist.github.com/jonschlinkert/e30c70c713da325d0e81