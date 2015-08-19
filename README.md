<a name="logo"/>
<div align="center">
<a href="http://julialang.org/" target="_blank">
<img src="http://julialang.org/images/logo_hires.png" alt="Julia Logo" width="210" height="142"></img>
</a>
</div>

# Contributing To Julia

This document tracks some ways to get involved in the Julia ecosystem - the language itself,
packages, educational material, and more. You can contribute to this document by
[editing this file](https://github.com/IainNZ/ContributeToJulia/edit/master/README.md)
in your browser and submitting a pull request.

###  Some concepts and terminology

**Testing**: One way to make sure code works in the way we intend is to write *tests*.
Testing in Julia involves writing code that tries out various different inputs to your
functions, and makes sure the that the outputs are what we expect.
Tests for Julia packages (and Julia itself) live in their `test/` subdirectories, and
the tests may span many files. Whenever we refactor our code, we can have some confidence
that we didn't introduce bugs if the tests still pass. If we fix a bug, we can add a
new test to make sure further work doesn't reintroduce the bug. Finally, if we add
a new feature we aim to make sure that there are tests for it.

**Continuous integration**: While we could rely on contributors running tests before
they submit changes, there can be various reasons why even if someone does run tests
that the changes might not work on another machine. Julia and many packages use at
least one *continuous integration* service to ensure that all changes pass tests
at all times. These services automatically pull the code from Github and run the
tests on fresh virtual machine, and then report back whether they failed or not.
The popular service is [TravisCI](http://travis-ci.org), and packages will often have
a "badge" like this:
[![Build Status](https://travis-ci.org/JuliaLang/JSON.jl.svg)](https://travis-ci.org/JuliaLang/JSON.jl))
in their README to show their tests are passing (or not).

  * Even if tests are passing, the tests may not be checking all possible ways the package can
    be used - possibly missing broken code! Julia can track which lines of code are executed in
    the package in the course of running the existing tests (the "test coverage"). Many packages
    automatically track their coverage using the [Coverage.jl](https://github.com/IainNZ/Coverage.jl)
    package and websites like [Codecov.io](http://codecov.io), and put a "badge" in their READMEs to
    track their coverage percentage (like this:
      [![JSON.jl's coverage](http://codecov.io/github/JuliaLang/JSON.jl/coverage.svg?branch=master)](http://codecov.io/github/JuliaLang/JSON.jl?branch=master)).
    You can also get coverage reports locally by passing the `--code-coverage` flag to Julia
    when running test scripts - see Coverage.jl's README for more help.
    **You can contribute tests to improve test coverage**



## Help out with Julia itself

Developing new features or fixing bugs can be a tough way start, so we recommend getting
started by adding "tests" - and Julia needs lots of tests!
We have an [issue](https://github.com/JuliaLang/julia/issues/11885)
open about Julia's test coverage to help you get started and to track overall progress.

## Help out with core packages

Julia includes a standard library, `Base`, with a lot of useful functionality.
Lots of important functionality lives outside of `Base` in various packages, many of which
are small enough for even a new user to understand. Contributing to these packages will
benefit large numbers of people, as they are depended on by large numbers of other packages
directly and indirectly.


### Packages looking for contributors

#### [JuliaWeb/URIParser.jl](https://github.com/JuliaWeb/URIParser.jl)

This package parses Uniform Resource Identifiers (URIs).
More packages directly or indirectly dependent on this package than any other!

#### [staticfloat/SHA.jl](https://github.com/staticfloat/SHA.jl)

This package implements the "SHA" family of hashing functions.
The second-most depedended-on package.
