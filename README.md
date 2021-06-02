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

# Constant Function

> Constant function.

<section class="intro">

A [constant function][constant-function] is a `function` whose output value is the same for every input value.

</section>

<!-- /.intro -->

<section class="installation">

## Installation

```bash
npm install @stdlib/utils-constant-function
```

</section>

<section class="usage">

## Usage

```javascript
var constantFunction = require( '@stdlib/utils-constant-function' );
```

#### constantFunction( x )

Returns a [constant function][constant-function] which always returns `x`.

```javascript
var fcn = constantFunction( 'beep' );
// returns <Function>

var v = fcn();
// returns 'beep'

v = fcn();
// returns 'beep'
```

</section>

<!-- /.usage -->

<section class="notes">

## Notes

-   When provided an object reference, the returned `function` always returns the same reference.

    ```javascript
    var obj = {};
    var fcn = constantFunction( obj );

    var bool = ( fcn() === obj );
    // returns true
    ```

</section>

<!-- /.notes -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```javascript
var constantFunction = require( '@stdlib/utils-constant-function' );

var bool;
var fcn;
var arr;
var v;
var i;

fcn = constantFunction( 3.14 );
for ( i = 0; i < 10; i++ ) {
    v = fcn();
    // returns 3.14
}

arr = [ 1, 2, 3 ];
fcn = constantFunction( arr );
for ( i = 0; i < 10; i++ ) {
    v = fcn();
    bool = ( v === arr );
    // returns true
}
```

</section>

<!-- /.examples -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/utils-constant-function/main/LICENSE

[constant-function]: https://en.wikipedia.org/wiki/Constant_function

</section>

<!-- /.links -->