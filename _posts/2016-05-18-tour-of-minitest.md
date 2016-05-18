---
layout: post
title: "A tour of MiniTest "
date:  2016-05-18 14:16:49
categories: ruby minitest
published: false  
---

[MiniTest](https://github.com/seattlerb/minitest) provides a complete suite of testing facilities supporting TDD, BDD, mocking, and benchmarking.

minitest/unit is a small and incredibly fast unit testing framework. It provides a rich set of assertions to make your tests clean and readable.

minitest/spec is a functionally complete spec engine. It hooks onto minitest/unit and seamlessly bridges test assertions over to spec expectations.

minitest/benchmark is an awesome way to assert the performance of your algorithms in a repeatable manner. Now you can assert that your newb co-worker doesn't replace your linear algorithm with an exponential one!

minitest/mock by Steven Baker, is a beautifully tiny mock (and stub) object framework.

minitest/pride shows pride in testing and adds coloring to your test output. I guess it is an example of how to write IO pipes too. :P

minitest/unit is meant to have a clean implementation for language implementors that need a minimal set of methods to bootstrap a working test suite. For example, there is no magic involved for test-case discovery.

minitest doesn't reinvent anything that ruby already provides, like: classes, modules, inheritance, methods. This means you only have to learn ruby to use minitest and all of your regular OO practices like extract-method refactorings still apply.

## Further reading
* [MiniTest Documentation](http://docs.seattlerb.org/minitest/)
* [MiniTest cheat sheat](http://danwin.com/2013/03/ruby-minitest-cheat-sheet/)
