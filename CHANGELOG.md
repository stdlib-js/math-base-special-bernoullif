# CHANGELOG

> Package changelog.

<section class="release" id="unreleased">

## Unreleased (2025-08-27)

<section class="features">

### Features

-   [`7d671b1`](https://github.com/stdlib-js/stdlib/commit/7d671b11b736366d61848f8b9014d5067825e39a) - add `math/base/special/bernoullif` [(#3037)](https://github.com/stdlib-js/stdlib/pull/3037)

</section>

<!-- /.features -->

<section class="breaking-changes">

### BREAKING CHANGES

-   [`59f0fbb`](https://github.com/stdlib-js/stdlib/commit/59f0fbbf7f8d36265950fcedc893f66d4691157f): update signature to accept floats

    -   User code should behave similarly in the primary case of providing integer-valued input values. However, no longer will real-values truncate. Now, real-valued inputs will result in `NaN`, which is, arguably, better behavior, as real-to-integer truncation can be a source of silent bugs.

</section>

<!-- /.breaking-changes -->

<section class="commits">

### Commits

<details>

-   [`81f904d`](https://github.com/stdlib-js/stdlib/commit/81f904da25808197e2ae83ebf9c8b26860855e7c) - **bench:** fix failing C benchmarks by using `round` and `roundf` [(#7980)](https://github.com/stdlib-js/stdlib/pull/7980) _(by Gunj Joshi)_
-   [`59f0fbb`](https://github.com/stdlib-js/stdlib/commit/59f0fbbf7f8d36265950fcedc893f66d4691157f) - **refactor:** modify C implementation to accept `float` instead of `int32` in `math/base/special/bernoullif` [(#7941)](https://github.com/stdlib-js/stdlib/pull/7941) _(by Gunj Joshi, Athan Reines)_
-   [`97ab65f`](https://github.com/stdlib-js/stdlib/commit/97ab65f9a65c9f1510f21309ff4892c752910e0f) - **docs:** fix missing closing section _(by Athan Reines)_
-   [`7d671b1`](https://github.com/stdlib-js/stdlib/commit/7d671b11b736366d61848f8b9014d5067825e39a) - **feat:** add `math/base/special/bernoullif` [(#3037)](https://github.com/stdlib-js/stdlib/pull/3037) _(by Gururaj Gurram, Athan Reines, stdlib-bot, Gunj Joshi, Karan Anand, Philipp Burckhardt)_

</details>

</section>

<!-- /.commits -->

<section class="contributors">

### Contributors

A total of 5 people contributed to this release. Thank you to the following contributors:

-   Athan Reines
-   Gunj Joshi
-   Gururaj Gurram
-   Karan Anand
-   Philipp Burckhardt

</section>

<!-- /.contributors -->

</section>

<!-- /.release -->

