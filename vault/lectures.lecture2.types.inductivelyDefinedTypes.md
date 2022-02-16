---
id: xYcRvblnuVYyHplhMk1Yr
title: Inductively Defined Types
desc: ''
updated: 1644996349500
created: 1644995841254
---
The algebraic types can be used like enums:

![](/assets/images/2022-02-16-08-11-30.png)

It is also possible to do pattern matching:
![](/assets/images/2022-02-16-08-11-57.png)

It is possible to declare multiple types under a specific type. We do so by denoting the type declaration with `|`.

![](/assets/images/2022-02-13-13-29-48.png)
>**Note:** that the declaration uses the `of` keyword to tell which sort of types it represents.

It is also possible to create some function which returns the value:
    
![](/assets/images/2022-02-16-08-13-05.png)

# Recursion
You can also recur the inductively defined types:

![](/assets/images/2022-02-16-08-22-37.png)
