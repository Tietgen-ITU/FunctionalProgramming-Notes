---
id: RoRO0qLBH4wZzjhcrTkpk
title: Functions
desc: 'How to declare functions'
updated: 1643907674607
created: 1643820453284
---
When you declare a method you then do it with the `let` keyword.
What follows afterwards are the name of the method and then the input parameters.

Just like when you declare a normal variable. 

Here is an example of how to declare a method

```F#
let circleArea rad = System.Math.PI * rad * rad
```
This function will be described as following: `val circleArea : float -> float`
The describtion basically says that the value circleArea is a type of `float -> float`. 

This means that the value circleArea is a function denoted by '->' with the first float as a parameter and the return type as a float.

## Returning a value
Functions return a value by taking the last line of the function. There is no keyword like the `return` in C# and Java. 