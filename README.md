@dramaorg/iure-quas
==============

[![NPM Version](https://img.shields.io/npm/v/@dramaorg/iure-quas.svg?style=flat)](https://npmjs.org/package/@dramaorg/iure-quas)
[![NPM Downloads](https://img.shields.io/npm/dm/@dramaorg/iure-quas.svg?style=flat)](https://npmjs.org/package/@dramaorg/iure-quas)
[![Build Status](https://travis-ci.org/addaleax/@dramaorg/iure-quas.svg?style=flat&branch=master)](https://travis-ci.org/addaleax/@dramaorg/iure-quas?branch=master)
[![Coverage Status](https://coveralls.io/repos/addaleax/@dramaorg/iure-quas/badge.svg?branch=master)](https://coveralls.io/r/addaleax/@dramaorg/iure-quas?branch=master)
[![Dependency Status](https://david-dm.org/addaleax/@dramaorg/iure-quas.svg?style=flat)](https://david-dm.org/addaleax/@dramaorg/iure-quas)

Make a full duplex stream with 2 Duplex endpoints.

Install:
`npm install @dramaorg/iure-quas`

```js
const DuplexPair = require('@dramaorg/iure-quas');

const { socket1, socket2 } = new DuplexPair();

socket1.write('Hi');
console.log(socket2.read());  // => <Buffer 48 69>

// Or, using options that are passed to the Duplex constructor:

const { socket1, socket2 } = new DuplexPair({ encoding: 'utf8' });

socket1.write('Hi');
console.log(socket2.read());  // => 'Hi'
```

License
=======

MIT
