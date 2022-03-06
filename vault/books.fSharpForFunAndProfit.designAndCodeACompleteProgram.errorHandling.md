---
id: a0pukcgwpo5fouluxucb17z
title: Error Handling
desc: ''
updated: 1646561224948
created: 1646560505095
---
When there is more than one way of outputing the success or failure of a function then it is hard to figure our if it worked or not. 
In functional programming we can make the use of [[Union types|lectures.lecture2.types.inductivelyDefinedTypes]]. 

![](/assets/images/2022-03-06-10-58-03.png)

However, it seems a bit comprehensive to add a new type when there can be a possibility of a new error. 
So we can simplify it a bit.

If we look at it a bit simplistic then we only have two different types of output

![](/assets/images/2022-03-06-11-00-01.png)

But there is no data in this kind of type. Therefor we can declare a type which can then compose some kind of data in case if it is either an error or a success:

![](/assets/images/2022-03-06-11-01-04.png)

So now the output looks like this:

![](/assets/images/2022-03-06-11-01-19.png)

This combines the errors from each step to a single "failure" path.

# Note
There already exists such a type and it is called [Choice](https://fsharp.github.io/fsharp-core-docs/reference/fsharp-core-fsharpchoice-2.html#Choice1Of2)
