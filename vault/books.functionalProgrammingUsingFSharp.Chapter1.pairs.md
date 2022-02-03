---
id: CutJv8SNUvqQptxWNACEM
title: Pairs
desc: This is notes about pairs in functional programming
updated: 1643920445244
created: 1643909673132
---
Pairs is a way to declare a tuple value e.g. ($val_1$, $val_2$). In F# this will be shown/described as `val1 * val2`.
![](/assets/images/2022-02-03-18-44-14.png)

Here is a code example:
```F#
let a = (3.0, 3)
```

This value is described as type like this (float * value):
```F#
val a = (2.0, 3) : float * int
```
>**Note:**
>Do you notice the `*`? It symbolizes that the value is a type from the cartesian product of the two values. In this case float and int

## Patterns
It is possible to create two new variables based on pattern. So taken from the example before with the variable `a` you can create two new variables like the following:
```F#
let (x, y) = a
```

This creates the following two new variables described as the following:
```F#
val y : int = 3
val x : float = 2.0
```


It is also a possibility to use pattern matching like the following:
![](/assets/images/2022-02-03-18-53-44.png)

> **Note:**
> It is important to note that the order of the clause is important. It is essential that the `(x, 0)` is first because if `(x, n)` was first then the `(x, 0)` would never have been evaluated.
> It evaluates the expressions from top to bottom.  