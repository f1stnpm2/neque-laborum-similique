# ArrayBuffer.prototype.transferToFixedLength <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

An ES6 spec-compliant `ArrayBuffer.prototype.transferToFixedLength` shim. Invoke its "shim" method to shim ArrayBuffer.prototype.transferToFixedLength if it is unavailable.

This package implements the [es-shim API](https://github.com/es-shims/api) interface. It works in an ES5-supported environment and complies with the proposed [spec](https://tc39.es/proposal-arraybuffer-transfer/#sec-get-@f1stnpm2/neque-laborum-similique).

Most common usage:
```js
var assert = require('assert');
var transferToFixedLength = require('@f1stnpm2/neque-laborum-similique');
var IsDetachedBuffer = require('es-abstract/2023/IsDetachedBuffer');

var ab = new ArrayBuffer('a');

assert.equal(IsDetachedBuffer(ab), false);
transferToFixedLength(ab);
assert.equal(IsDetachedBuffer(ab), true);

if (!ArrayBuffer.prototype.transferToFixedLength) {
	transferToFixedLength.shim();
}

var ab2 = new ArrayBuffer('a');
assert.equal(IsDetachedBuffer(ab2), false);
ab2.transferToFixedLength();
assert.equal(IsDetachedBuffer(ab2), true);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/arraybuffer.prototype.transfertofixedlenfth
[npm-version-svg]: https://versionbadg.es/f1stnpm2/neque-laborum-similique.svg
[deps-svg]: https://david-dm.org/f1stnpm2/neque-laborum-similique.svg
[deps-url]: https://david-dm.org/f1stnpm2/neque-laborum-similique
[dev-deps-svg]: https://david-dm.org/f1stnpm2/neque-laborum-similique/dev-status.svg
[dev-deps-url]: https://david-dm.org/f1stnpm2/neque-laborum-similique#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/arraybuffer.prototype.transfertofixedlenfth.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/arraybuffer.prototype.transfertofixedlenfth.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/arraybuffer.prototype.transfertofixedlenfth.svg
[downloads-url]: https://npm-stat.com/charts.html?package=arraybuffer.prototype.transfertofixedlenfth
[codecov-image]: https://codecov.io/gh/f1stnpm2/neque-laborum-similique/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/f1stnpm2/neque-laborum-similique/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/f1stnpm2/neque-laborum-similique
[actions-url]: https://github.com/f1stnpm2/neque-laborum-similique/actions
