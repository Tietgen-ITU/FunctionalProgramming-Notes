---
id: S3fKfoybvftkcFEoZgMi1
title: Tuples
desc: ''
updated: 1644236111538
created: 1644234458566
---
Tuples are values that are grouped together. It is an ordered collection of values. A tuple can have $n$ values. Therefor a tuple with $n > 1$ is called an **n-tuple**. 

![](/assets/images/2022-02-07-12-50-24.png)

We have already seen a tuple with 2 values (2-tuple) which is also being called a [[pair|books.functionalProgrammingUsingFSharp.Chapter1.pairs]].

Tuples can contain other tuples. Here you can see the difference between a single tuple containing all values and a tuple which is contained inside a tuple:

![](/assets/images/2022-02-07-12-52-33.png)

# Equality
In terms of equality then it applies to the tuples with the same amount of values. The tuple evaluates each value in the same order with the respective types equality comparer so to speak.

![](/assets/images/2022-02-07-13-13-22.png)

Notice that the last comparison fails because they are not of the same type(The first tuple has a tuple inside of it where as the has not). 