# PCG Random Number Generation, C++ Edition

[PCG-Random website]: http://www.pcg-random.org

This code provides an implementation of the PCG family of random number
generators, which are fast, statistically excellent, and offer a number of
useful features.

Full details can be found at the [PCG-Random website].  This version
of the code provides many family members -- if you just want one
simple generator, you may prefer the minimal C version of the library.

There are two kinds of generator, normal generators and extended generators.
Extended generators provide *k* dimensional equidistribution and can perform
party tricks, but generally speaking most people only need the normal
generators.

There are two ways to access the generators, using a convenience typedef
or by using the underlying templates directly (similar to C++11's `std::mt19937` typedef vs its `std::mersenne_twister_engine` template).  For most users, the convenience typedef is what you want, and probably you're fine with `pcg32` for 32-bit numbers.  If you want 64-bit numbers, either use `pcg64` (or, if you're on a 32-bit system, making 64 bits from two calls to `pcg32_k2` may be faster).

## Documentation and Examples

Visit [PCG-Random website] for information on how to use this library, or look
at the sample code in the `sample` directory -- hopefully it should be fairly
self explanatory.
