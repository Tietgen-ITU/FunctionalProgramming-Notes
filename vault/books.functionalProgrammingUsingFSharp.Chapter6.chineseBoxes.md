---
id: u4r7syGzPD05RrQ3ijLI4
title: Chinese Boxes
desc: ''
updated: 1644755062733
created: 1644694391707
---
In order to create a data structure of the chineses box then we have the following rules to follow:

![](/assets/images/2022-02-13-13-15-12.png)
![](/assets/images/2022-02-13-13-15-33.png)

In order to create such data structure we can do the following:

![](/assets/images/2022-02-13-13-16-15.png)

This is a way to declare some sort of a tree structure. 

In order to create instances of it we do the following:

![](/assets/images/2022-02-13-13-17-37.png)

# Patterns
The rules in the pattern matching is that the cb value can either be of a type `Cube` or `Nothing`. Therefor we can easily declare the following pattern mathcing:
![](/assets/images/2022-02-13-13-20-24.png)

*To see more about pattern matching: [[Patterns|guides.patterns]]*

# Invariant function
There are also other rules to follow when creating the chineses boxes e.g. the float must be a postive value.

We can do so by declaring a instertion funtion:

![](/assets/images/2022-02-13-13-23-23.png)

And use the function like the following:
![](/assets/images/2022-02-13-13-24-02.png)