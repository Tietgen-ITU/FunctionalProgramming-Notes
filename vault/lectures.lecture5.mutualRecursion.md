---
id: is8fu4l3ejg4f6q696q86e9
title: Mutual Recursion
desc: ''
updated: 1646211165393
created: 1646210653057
---
The example of the bottom is a mutual recursive type:

![](/assets/images/2022-03-02-09-46-26.png)

![](/assets/images/2022-03-02-09-47-36.png)

>**Note:** that the `and` keyword sort of combines these two functions

However this implementation blow up our stack:

![](/assets/images/2022-03-02-09-52-01.png)

So we want to use continuation:

![](/assets/images/2022-03-02-09-52-29.png)