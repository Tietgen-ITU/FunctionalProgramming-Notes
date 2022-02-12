---
id: RE45VHW6ulIiWbuPAFEme
title: Types
desc: ''
updated: 1644402323585
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