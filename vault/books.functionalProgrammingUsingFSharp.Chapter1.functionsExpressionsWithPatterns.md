---
id: SQqHMbuyNrj3f4ZJBhAxm
title: Function Expressions With Patterns
desc: ''
updated: 1643910852904
created: 1643821895884
---
It is sometimes useful to define function in terms of cases e.g.
![](/assets/images/2022-02-02-18-15-23.png)

This function covers every month and is described formally as `val it : int -> int` (the name 'it' is a name given when in the interactive mode and a name is not declared).

You can also shorten this expression by using the or pattern e.g.
![](/assets/images/2022-02-02-18-27-14.png)

The `_` is a default. So if for example the function get called like `it 0` then it will return 31.

You can also name it like you do with a normal function like
![](/assets/images/2022-02-02-18-29-03.png)
