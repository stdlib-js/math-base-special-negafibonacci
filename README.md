<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

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

# negaFibonacci

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Compute the nth [negaFibonacci number][fibonacci-number].

<section class="intro">

The [negaFibonacci numbers][fibonacci-number] are the integer sequence

<!-- <equation class="equation" label="eq:negafibonacci_sequence" align="center" raw="0, 1, -1, 2, -3, 5, -8, 13, -21, 34, -55, 89, -144, \ldots" alt="NegaFibonacci sequence"> -->

<div class="equation" align="center" data-raw-text="0, 1, -1, 2, -3, 5, -8, 13, -21, 34, -55, 89, -144, \ldots" data-equation="eq:negafibonacci_sequence">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@bb29798906e119fcb2af99e94b60407a270c9b32/lib/node_modules/@stdlib/math/base/special/negafibonacci/docs/img/equation_negafibonacci_sequence.svg" alt="NegaFibonacci sequence">
    <br>
</div>

<!-- </equation> -->

The sequence is defined by the recurrence relation

<!-- <equation class="equation" label="eq:negafibonacci_recurrence_relation" align="center" raw="F_{n-2} = F_{n} - F_{n-1}" alt="NegaFibonacci sequence recurrence relation"> -->

<div class="equation" align="center" data-raw-text="F_{n-2} = F_{n} - F_{n-1}" data-equation="eq:negafibonacci_recurrence_relation">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@bb29798906e119fcb2af99e94b60407a270c9b32/lib/node_modules/@stdlib/math/base/special/negafibonacci/docs/img/equation_negafibonacci_recurrence_relation.svg" alt="NegaFibonacci sequence recurrence relation">
    <br>
</div>

<!-- </equation> -->

which yields

<!-- <equation class="equation" label="eq:negafibonacci_fibonacci" align="center" raw="F_{-n} = (-1)^{n+1} F_n" alt="NegaFibonacci relationship to Fibonacci numbers"> -->

<div class="equation" align="center" data-raw-text="F_{-n} = (-1)^{n+1} F_n" data-equation="eq:negafibonacci_fibonacci">
    <img src="https://cdn.jsdelivr.net/gh/stdlib-js/stdlib@bb29798906e119fcb2af99e94b60407a270c9b32/lib/node_modules/@stdlib/math/base/special/negafibonacci/docs/img/equation_negafibonacci_fibonacci.svg" alt="NegaFibonacci relationship to Fibonacci numbers">
    <br>
</div>

<!-- </equation> -->

with seed values `F_0 = 0` and `F_{-1} = 1`.

</section>

<!-- /.intro -->

<section class="installation">

## Installation

```bash
npm install @stdlib/math-base-special-negafibonacci
```

Alternatively,

-   To load the package in a website via a `script` tag without installation and bundlers, use the [ES Module][es-module] available on the [`esm` branch][esm-url].
-   If you are using Deno, visit the [`deno` branch][deno-url].
-   For use in Observable, or in browser/node environments, use the [Universal Module Definition (UMD)][umd] build available on the [`umd` branch][umd-url].

The [branches.md][branches-url] file summarizes the available branches and displays a diagram illustrating their relationships.

</section>

<section class="usage">

## Usage

```javascript
var negafibonacci = require( '@stdlib/math-base-special-negafibonacci' );
```

#### negafibonacci( n )

Computes the nth [negaFibonacci number][fibonacci-number].

```javascript
var v = negafibonacci( 0 );
// returns 0

v = negafibonacci( -1 );
// returns 1

v = negafibonacci( -2 );
// returns -1

v = negafibonacci( -3 );
// returns 2

v = negafibonacci( -78 );
// returns -8944394323791464
```

If `n < -78`, the function returns `NaN`, as larger [negaFibonacci numbers][fibonacci-number] cannot be safely represented in [double-precision floating-point format][ieee754].

```javascript
var v = negafibonacci( -79 );
// returns NaN
```

If not provided a nonpositive integer value, the function returns `NaN`.

```javascript
var v = negafibonacci( -3.14 );
// returns NaN

v = negafibonacci( 1 );
// returns NaN
```

If provided `NaN`, the function returns `NaN`.

```javascript
var v = negafibonacci( NaN );
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

```javascript
var negafibonacci = require( '@stdlib/math-base-special-negafibonacci' );

var v;
var i;

for ( i = 0; i > -79; i-- ) {
    v = negafibonacci( i );
    console.log( v );
}
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

* * *

## See Also

-   <span class="package-name">[`@stdlib/math/base/special/fibonacci`][@stdlib/math/base/special/fibonacci]</span><span class="delimiter">: </span><span class="description">compute the nth Fibonacci number.</span>
-   <span class="package-name">[`@stdlib/math/base/special/negalucas`][@stdlib/math/base/special/negalucas]</span><span class="delimiter">: </span><span class="description">compute the nth negaLucas number.</span>

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

Copyright &copy; 2016-2022. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/math-base-special-negafibonacci.svg
[npm-url]: https://npmjs.org/package/@stdlib/math-base-special-negafibonacci

[test-image]: https://github.com/stdlib-js/math-base-special-negafibonacci/actions/workflows/test.yml/badge.svg?branch=main
[test-url]: https://github.com/stdlib-js/math-base-special-negafibonacci/actions/workflows/test.yml?query=branch:main

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/math-base-special-negafibonacci/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/math-base-special-negafibonacci?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/math-base-special-negafibonacci.svg
[dependencies-url]: https://david-dm.org/stdlib-js/math-base-special-negafibonacci/main

-->

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/math-base-special-negafibonacci/tree/deno
[umd-url]: https://github.com/stdlib-js/math-base-special-negafibonacci/tree/umd
[esm-url]: https://github.com/stdlib-js/math-base-special-negafibonacci/tree/esm
[branches-url]: https://github.com/stdlib-js/math-base-special-negafibonacci/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/math-base-special-negafibonacci/main/LICENSE

[fibonacci-number]: https://en.wikipedia.org/wiki/Fibonacci_number

[ieee754]: https://en.wikipedia.org/wiki/IEEE_754-1985

<!-- <related-links> -->

[@stdlib/math/base/special/fibonacci]: https://github.com/stdlib-js/math-base-special-fibonacci

[@stdlib/math/base/special/negalucas]: https://github.com/stdlib-js/math-base-special-negalucas

<!-- </related-links> -->

</section>

<!-- /.links -->
