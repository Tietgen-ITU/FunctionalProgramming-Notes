---
id: 1K9CnHSrxiFBWnCdmB17j
title: List Recursion
desc: ''
updated: 1644299751098
created: 1644298890168
---
When doing recurssion on a list then we have the pattern from the section [[Pattern with lists|books.functionalProgrammingUsingFSharp.Chapter4.list#pattern]] being the `x::xs`. However we also have `[]` which symbolises the empty list.

This can make us do all sorts of things like the sum of all the values in the list:
![](/assets/images/2022-02-08-06-47-12.png)

We can also take more than one value out of the list and make it recursive by doing the following:
![](/assets/images/2022-02-08-06-49-18.png)

## Layered patterns
It is also possible to declare the value like the following pattern $x_0::x_1::xs$ while still having the $x_1$ in the xs variable.

We do so by layered patterns. It works by indicating that you want that value and then declaring it that it should be noticed as xs.
![](/assets/images/2022-02-08-06-53-25.png)

So now a function like the following can be created:
![](/assets/images/2022-02-08-06-54-16.png)
