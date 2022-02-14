---
id: RE45VHW6ulIiWbuPAFEme
title: Types
desc: ''
updated: 1644756279788
created: 1644392234536
---
It is possible to declare our own types.
We do so like in the following example:
![](/assets/images/2022-02-09-08-39-13.png)

Sometimes F# does not know that it should use your type like the following example:
![](/assets/images/2022-02-09-08-43-03.png)

But the two types we have defined use the `float * float * float` so the type can be used in the function any way.

An example of declaring and creating a variable of that type can be seen here:
```F#
type complex = float * float;;
let value = complex(2.0, 1.0);;
> val value : complex = (2.0, 1.0)
```
## Subtyping
It is possible to declare multiple types under a specific type. We do so by denoting the type declaration with `|`.

![](/assets/images/2022-02-13-13-29-48.png)
>**Note:** that the declaration uses the `of` keyword to tell which sort of types it represents.

# Why?
Why should we use types? It is a good way to use in pattern matching. It gives a good declarative sence of what we want and what we represent. 

A good example of that is the way to create an expression tree in F#.

![](/assets/images/2022-02-13-13-43-16.png)

By the type declaration from the "Subtyping" section we can declare recursive or tree structure like types. This gives a opportunity to create function that uses pattern matching:

![](/assets/images/2022-02-13-13-44-31.png)