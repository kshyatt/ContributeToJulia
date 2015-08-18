<a name="logo"/>
<div align="center">
<a href="http://julialang.org/" target="_blank">
<img src="http://julialang.org/images/logo_hires.png" alt="Julia Logo" width="210" height="142"></img>
</a>
</div>

# Contributing To Julia

This document tracks some ways to get involved in the Julia ecosystem - the language itself, packages, educational material, and more. You can contribute to this document by [editing this file](https://github.com/IainNZ/ContributeToJulia/edit/master/README.md) in your browser and submitting a pull request.

## Help out with core packages

Julia includes a standard library, `Base`, with a lot of useful functionality. Lots of important functionality lives outside of `Base` in various packages, many of which are small enough for even a new user to understand. Contributing to these packages will benefit large numbers of people, as they are depended on by large numbers of other packages directly and indirectly.

Ways you can contribute:
* **Add tests to improve test coverage**: the goal for any package should be that every line of code works correctly for all inputs. A good way to find out what needs tests is to look at the "code coverage": Julia can track which lines of code are executed in the package in the course of running the existing tests. Many packages automatically track their code coverage using the [Coverage.jl](https://github.com/IainNZ/Coverage.jl) package and websites like [Codecov.io](http://codecov.io), and put a "badge" in their READMEs to track their coverage percentage (like this: [![JSON.jl's coverage](http://codecov.io/github/JuliaLang/JSON.jl/coverage.svg?branch=master)](http://codecov.io/github/JuliaLang/JSON.jl?branch=master)). You can also get coverage reports locally by passing the `--code-coverage` flag to Julia when running test scripts - see Coverage.jl's README for more help.

#### 
