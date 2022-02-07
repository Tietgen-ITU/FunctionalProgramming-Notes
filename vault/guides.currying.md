---
id: qhUzznGZVUkxDJFnCXUnj
title: Currying
desc: ''
updated: 1644213445785
created: 1644213172029
---
Currying is the concept where you inject a function into another function which then returns a function.

Take a look at the following example:
```F#
let curry f x y = f(x, y);;
> val curry: f: ('a -> 'b -> 'c) -> x: 'a -> y: 'b -> 'c
```
As you can see here the curry method defines that it should take a function and return that function with a value in the end called `c`.

This is very useful in order to "extend" methods or to make them dynamic. 
