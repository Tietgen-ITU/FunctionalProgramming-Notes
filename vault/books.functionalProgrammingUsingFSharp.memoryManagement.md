---
id: 98z7uug8tsohvufs8su030e
title: Memory Management
desc: ''
updated: 1645953174596
created: 1645951327850
---
There is a **stack** and an **heap**. The primitive values are located and stored on the stack. The composite values are stored on the heap(i.e. lists, trees, closures, and most objects).

![](/assets/images/2022-02-27-09-44-36.png)

The important things to notice here is the following:

![](/assets/images/2022-02-27-09-47-13.png)

# Basic operations on the stack and heap
We are going to evaluate how the memory behaves on the following function:

![](/assets/images/2022-02-27-09-49-26.png)

We start with an empty stack frame. Nothing has been pushed to the stack other than it knows that the function is called `zs`.

#### Pushing a stack frame
![](/assets/images/2022-02-27-09-50-14.png)

The start of the evaluation of the local declarations will push an new stack frame on top of the function `sf_0`. The stack frames has entries for the locally declarared variables `xs` and `ys` and also some extra entries including one for the `result` of the local expression `xs @ ys`

#### Popping a stack frame
![](/assets/images/2022-02-27-09-57-12.png)

When the result of the expression `xs @ ys` has been computed, then the stack frame `sf_1` is popped, that is removed from the stack, and the reference to the first cons cell of `xs @ ys` is copied to the stack entry for `zs`.

It is important to notice that the heap has marked two objects for deletion e.i. the one that is at the top of the heap. 
When the stack has popped its bindings to the values in the heap, the heap then marks objects that are not being referenced anymore for deletiong. The **garbage collector** can then remove the items later.

# Heap
Some information about the heap is that it categorizes objects into three generations:
- Gen0 - young objects
- Gen1 - not that young objects but not too old either
- Gen2 - old objects

The typical situation is that objects die young. Garbage collection typically occurs among young objects and the garbage collector. The garbage collector is designed for that. 

# The limits of the stack and the heap
The maximal heap size is order of magnitude larger than the maximal stack size.

![](/assets/images/2022-02-27-10-10-01.png)

Notice that the stack limit is pretty small compared to the other list we now are going to create:

![](/assets/images/2022-02-27-10-12-50.png)