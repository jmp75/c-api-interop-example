# c-api-interop-example

Introductory example for surfacing a C API to R, Python, Matlab, etc.

Take home messages to aim for:

* generate bindings
* Reasons why a C API remains necessary. Cite the example with Rtools.

Structurally what to aim for:

* A C++ core
* Cross-module interop: two libraries with a dependency
* A C API exposing base C99 types (ANSI C), structs and C++ objects as `void*`
* Directly beneath the C API, using reference counter wrappers around C++ objects on the heap (i.e. created for and then manipulated by external R/Python/etc. bindings)

Progression of the tutorial:

* Existing setup; no support for reference counting in the core libraries.
* Creating bindings; use R as an example
* Illustrate the shortcomings of "naked" pointers.
* introduce reference counters
