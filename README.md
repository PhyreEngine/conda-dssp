This repository contains a [conda][conda] recipe for building
[DSSP][dssp], a tool for sequence-dependent protein structural
alignment.

## Prerequisites

1. You will need an installation of [conda][miniconda].

2. Your root conda installation must have the `conda-build` installed.

## Building

You should be able to build this package by simply running `conda build .`.

## Patches

This recipe applies two patches:

`makefile.patch`
    This patch alters the supplied Makefile to play nicely with `conda build`.
    The patch allows `conda build`'s environment variables to pass through,
    and writes the man page to `$PREFIX/share/man`.

`tuple.patch`
    Removes obsolete references to `std::tr1::tuple`, replacing them with
    `std::tuple`.

[conda]: https://conda.io
[dssp]: http://swift.cmbi.ru.nl/gv/dssp/
[miniconda]: https://conda.io/miniconda.html
