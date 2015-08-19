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

## Help out with base Julia

Julia needs lots of tests! We have an [issue](https://github.com/JuliaLang/julia/issues/11885)
open about Julia's test coverage to help you get started and track our progress.

## Help out with core packages

Julia includes a standard library, `Base`, with a lot of useful functionality.
Lots of important functionality lives outside of `Base` in various packages, many of which
are small enough for even a new user to understand. Contributing to these packages will
benefit large numbers of people, as they are depended on by large numbers of other packages
directly and indirectly.

Ways you can contribute:
* **Add tests**.
  The goal for any package should be that every line of code works correctly for all inputs.
  One way to achieve this goal is to use "tests", code that ensures the package works as described.
  Tests for Julia packages live in the `test/` subdirectory for a package, and may span many files.
  * Many packages use "continuous integration" to ensure that they are always passing tests.
    Almost all registered Julia packages use [TravisCI](http://travis-ci.org) to automatically
    run their tests whenever a change is pushed to the package on Github. Packages will often have
    a "badge" (like this: 
      [![Build Status](https://travis-ci.org/JuliaLang/JSON.jl.svg)](https://travis-ci.org/JuliaLang/JSON.jl))
    that show whether tests are passing.
    **If you see that tests aren't passing, try to identify the problem and submit a fix.**
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

### Packages looking for contributors

#### [JuliaWeb/URIParser.jl](https://github.com/JuliaWeb/URIParser.jl)

This package parses Uniform Resource Identifiers (URIs).
More packages directly or indirectly dependent on this package than any other!

#### [staticfloat/SHA.jl](https://github.com/staticfloat/SHA.jl)

This package implements the "SHA" family of hashing functions.
The second-most depedended-on package.
