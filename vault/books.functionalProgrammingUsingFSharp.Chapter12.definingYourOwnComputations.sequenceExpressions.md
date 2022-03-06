---
id: 0318q2mhy4nmbzzy7jz1iqj
title: Sequence Expressions
desc: ''
updated: 1646555779547
created: 1646554285349
---
The `seq` expression is an expression that does something sequentially.

You could create an expression that creates tuples with the different values. Then you can create the following:
```F#
let pairRecipe = seq {for i in seq [1 .. 3] do
                           for ch in seq [’a’ .. ’d’] do
                              yield (i,ch) };;

val pairRecipe : seq<int * char>
```
>**Note:** that the type generated from this is a computation type `seq`. You maybe notice that you did not get the values.
>That is because of the nature of computations. They work a bit like the `IEnumerable` type from C#. There it only yields you the computation when you iterated through the `IEnumerable`. This is basically the same concept. Here it only gives you the result when you ask for the result.


The construct of this is like the following:

![](/assets/images/2022-03-06-09-20-56.png)

The $ce(i)$ means the next computation in the sequence of elements.

#### Example of computation
![](/assets/images/2022-03-06-09-35-11.png)
![](/assets/images/2022-03-06-09-35-17.png)
