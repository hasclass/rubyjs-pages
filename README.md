---
layout: post
title: RubyJS
---

#### State of this project:

This project is pre-alpha (whatever that means). Implemented are roughly 80% of the methods from Array, Enumerable, String, Range, Numeric, Float, Integer. Check the current progress in progress.txt. Most big issues have been solved and I am finishing the remaining methods, trying to find the right tradeoffs and smart ways to package things together.

## RubyJS

A port of the Ruby 1.9.3 corelib to coffeescript/javascript/node that conforms to rubyspec.org and does not pollute the global javascript namespace. It is not an attempt to port or mimic the ruby object model and metaprogramming capabilities, whatsoever. 

Why? Coffeescript made it easy to switch from ruby/python. Unfortunately I quickly missed the functionality of the ruby corelib (the very core part of it, String, Array, Numeric, etc.). 

In numbers (as of 2012-07-25): 230 methods, 900 specs, gzipped ~10kb, minified ~40kb.

### Features

- Methods comply 1 to 1 to ruby code (tested by ~1000 rubyspec tests), down to raising the same Error types. 
- All methods of the core ruby classes, excluding ruby specifics and bit operators.
- Enumerators, Iterators, Enumerable. Chainable and extendible.
- Consistent breaking out of loops using: catch_break (breaker) -> breaker.break().
- Methods automatically box/coerce native JS primitives into the right RubyJS type.
- Small filesize: 10-20kb minified and gzipped.

### RubyJS Code samples

