---
id: 3hXW8VEIs5OLWKfUVcZ9r
title: List
desc: ''
updated: 1644398068565
created: 1644257873523
---
When we want to declare a list then we can do the following:
![](/assets/images/2022-02-07-19-18-19.png)

However sometimes we want a more complex list with a more complex type:

![](/assets/images/2022-02-07-19-19-01.png)

We can also declare list with functions in it:

![](/assets/images/2022-02-07-19-19-28.png)

The list is shown like a graph or more like a tree:
![](/assets/images/2022-02-08-06-22-21.png)

The `::` in this example is called a tagged pair. It has a reference to a value(the left side) called head and a reference to the rest of the list(on the right side). 

## Construction and decomposition of lists
Before the following symbol `::` was called a tagged pair. However in this instance it is an infix operator called cons. Cons builds a list from its head and its tail as shown in the following example:

![](/assets/images/2022-02-08-06-25-56.png)

The operator associates to the right. so $x_0::x_1::xs$ which really means that $x_0::(x_1::xs)$ because $x_0$ and $x_1$ has the value and $xs$ is a list of the rest of the values. The parenthesis indicates that it is a list from the tail of the $x_0$ is you can say so. Just like in the following figure:
![](/assets/images/2022-02-08-06-30-10.png)

## Pattern 
It is also possible to assign values based on a pattern from the list.
As you can see here the `x::xs` pattern will assign the first value to an  `x` variable and the rest of the list to `xs`:

![](/assets/images/2022-02-08-06-33-39.png)

You can also do so with more values and or use pairs:
![](/assets/images/2022-02-08-06-34-41.png)

## List Expressions
We can also generate a list by the following:
![](/assets/images/2022-02-08-06-36-15.png)

It illustrates an example of how to create a list from a specific value to another value.

This can also be done by using the some sort of expression like:
![](/assets/images/2022-02-08-06-37-09.png)

>**Note:** that the value here $3.0 ** 1.7 = 647300784$ hence the next value of the above list is not being added.

The list can be ascending or descending. And you can declare how much the value should be added too:
![](/assets/images/2022-02-08-06-39-30.png)
>**Note:** the $-1$ value in the middle indicates that the value should descend by $1$ the value could have been $2$ or $-3$.

## Append lists
It is also a possibility to append to lists together we can do so by using the `List.append` function or use the infix operator `@`.
The append function can be used like the following example:
![](/assets/images/2022-02-09-09-09-40.png)

The infix `@` is implemented in the following way:
![](/assets/images/2022-02-08-07-02-20.png)
![](/assets/images/2022-02-08-07-02-29.png) 