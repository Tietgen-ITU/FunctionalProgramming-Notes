---
id: FybaQrn7HhPUTqiGvE0MP
title: Locations
desc: ''
updated: 1645198352864
created: 1645197097769
---
A *Location* is a variable that can be changed.

You can declare a location by the following:
```F#
let mutable x = 1;

x <- 2
```

We do it by using the `mutable` keyword.

![](/assets/images/2022-02-18-16-23-44.png)

A mutable declaration requires an initial value.
When you do not have an initial value then you can use the following `Unchecked.defaultOf<type>`.

