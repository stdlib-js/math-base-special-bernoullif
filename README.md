<!--

@license Apache-2.0

Copyright (c) 2025 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# bernoullif

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Compute the nth [Bernoulli number][bernoulli-number] as a single-precision floating-point number.

<section class="intro">

</section>

<!-- /.intro -->



<section class="usage">

## Usage

To use in Observable,

```javascript
bernoullif = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-bernoullif@umd/browser.js' )
```
The previous example will load the latest bundled code from the umd branch. Alternatively, you may load a specific version by loading the file from one of the [tagged bundles](https://github.com/stdlib-js/math-base-special-bernoullif/tags). For example,

```javascript
bernoullif = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-bernoullif@v0.1.0-umd/browser.js' )
```

To vendor stdlib functionality and avoid installing dependency trees for Node.js, you can use the UMD server build:

```javascript
var bernoullif = require( 'path/to/vendor/umd/math-base-special-bernoullif/index.js' )
```

To include the bundle in a webpage,

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-bernoullif@umd/browser.js"></script>
```

If no recognized module system is present, access bundle contents via the global scope:

```html
<script type="text/javascript">
(function () {
    window.bernoullif;
})();
</script>
```

#### bernoullif( n )

Computes the nth [Bernoulli number][bernoulli-number] as a single-precision floating-point number.

```javascript
var v = bernoullif( 0 );
// returns 1.0

v = bernoullif( 1 );
// returns 0.5

v = bernoullif( 2 );
// returns ~0.167

v = bernoullif( 3 );
// returns 0.0

v = bernoullif( 4 );
// returns ~-0.033

v = bernoullif( 5 );
// returns 0.0

v = bernoullif( 20 );
// returns ~-529.124
```

For even integers `n >= 66`, the function alternates between returning positive and negative infinity, as larger [Bernoulli numbers][bernoulli-number] cannot be safely represented in [single-precision floating-point format][ieee754].

```javascript
var v = bernoullif( 66 );
// returns Infinity

v = bernoullif( 68 );
// returns -Infinity

v = bernoullif( 70 );
// returns Infinity
```

If not provided a nonnegative integer value, the function returns `NaN`.

```javascript
var v = bernoullif( 3.14 );
// returns NaN

v = bernoullif( -1 );
// returns NaN
```

If provided `NaN`, the function returns `NaN`.

```javascript
var v = bernoullif( NaN );
// returns NaN
```

</section>

<!-- /.usage -->

<section class="notes">

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/console-log-each-map@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/random-array-discrete-uniform@umd/browser.js"></script>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/math-base-special-bernoullif@umd/browser.js"></script>
<script type="text/javascript">
(function () {

var x = discreteUniform( 100, 0, 70, {
    'dtype': 'int32'
});

logEachMap( 'bernoullif(%d) = %0.4f', x, bernoullif );

})();
</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- C interface documentation. -->



<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2026. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/math-base-special-bernoullif.svg
[npm-url]: https://npmjs.org/package/@stdlib/math-base-special-bernoullif

[test-image]: https://github.com/stdlib-js/math-base-special-bernoullif/actions/workflows/test.yml/badge.svg?branch=v0.1.0
[test-url]: https://github.com/stdlib-js/math-base-special-bernoullif/actions/workflows/test.yml?query=branch:v0.1.0

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/math-base-special-bernoullif/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/math-base-special-bernoullif?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/math-base-special-bernoullif.svg
[dependencies-url]: https://david-dm.org/stdlib-js/math-base-special-bernoullif/main

-->

[chat-image]: https://img.shields.io/badge/zulip-join_chat-brightgreen.svg
[chat-url]: https://stdlib.zulipchat.com

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/math-base-special-bernoullif/tree/deno
[deno-readme]: https://github.com/stdlib-js/math-base-special-bernoullif/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/math-base-special-bernoullif/tree/umd
[umd-readme]: https://github.com/stdlib-js/math-base-special-bernoullif/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/math-base-special-bernoullif/tree/esm
[esm-readme]: https://github.com/stdlib-js/math-base-special-bernoullif/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/math-base-special-bernoullif/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/math-base-special-bernoullif/main/LICENSE

[bernoulli-number]: https://en.wikipedia.org/wiki/Bernoulli_number

[ieee754]: https://en.wikipedia.org/wiki/IEEE_754-1985

</section>

<!-- /.links -->
