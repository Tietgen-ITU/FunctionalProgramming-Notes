---
id: 8potyttz5chg2um4feaeaq1
title: Memory Model
desc: ''
updated: 1646206202114
created: 1646204665787
---
This builds on [[books.functionalProgrammingUsingFSharp.memoryManagement]].

We consider the following function:

![](/assets/images/2022-03-02-08-06-00.png)

This expression cannot be evaluated before we reach the base case. All of these results and computations that cannot be completed must be keept in memory.

![](/assets/images/2022-03-02-08-09-23.png)

So for larger numbers in the `fact` function will throw `StackOverflow`.

# Model of the memory in F#
![](/assets/images/2022-03-02-08-10-35.png)
![](/assets/images/2022-03-02-08-10-56.png)
Notice here that it does not copied however it just continues and points to the next list.

## Stack Frames
![](/assets/images/2022-03-02-08-14-12.png)

When everything is done then we will pop the stack frame:

![](/assets/images/2022-03-02-08-14-45.png)

>**Note:** that there are marked parts of the heap that is not reachable. It will later be collected by the Garbage Collector.

![](/assets/images/2022-03-02-08-16-08.png)

# Examples
![](/assets/images/2022-03-02-08-19-35.png)

## List append
![](/assets/images/2022-03-02-08-20-04.png)
![](/assets/images/2022-03-02-08-20-34.png)

But the built-in list append function works??? 

![](/assets/images/2022-03-02-08-24-23.png)
Why?
Becuase the list append uses the heap instead of the stack. 

## List Reversal
![](/assets/images/2022-03-02-08-25-15.png)

This function is quadratic. 
