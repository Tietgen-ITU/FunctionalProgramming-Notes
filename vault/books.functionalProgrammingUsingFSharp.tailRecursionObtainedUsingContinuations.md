---
id: 9kqavjuer6qdv5pcmwq4x0b
title: Tail Recursion Obtained Using Continuations
desc: ''
updated: 1645954190157
created: 1645953851863
---
We can obtain tail recursion which is a fast form for recursion by using *continuation* function.

See the basic function here:
![](/assets/images/2022-02-27-10-27-30.png)

We modify this function to take in a function `c`.
![](/assets/images/2022-02-27-10-28-21.png)
