---
id: BqQNP5zYSpMBNsw0JlWxe
title: Recursion
desc: This page describes how to do recursion
updated: 1643909668770
created: 1643823048295
---
Recursive functions is a function which calls itself.
In f# you can only create a recursive function by declaring the function with the `rec` keyword. 

It is important to declare the recursive function with this keyword becuase the intelli sense can find the function other wise.

```F#
let rec someFunction <parameters> = <function logic>
```

**Example:**

Here is an example of a recursive function solving or calculating factorial (e.g. N!)
![](/assets/images/2022-02-03-17-52-57.png)

## Note
It is important to note that the variable or parameter `n` is declared in the function expression. Also the type is inferred by the first pattern matching `0` which is an int.

