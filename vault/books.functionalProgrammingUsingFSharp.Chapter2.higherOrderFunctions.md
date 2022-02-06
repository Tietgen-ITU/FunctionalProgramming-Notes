---
id: FjstSJv4zejYRgJldG6e4
title: Higher Order Functions
desc: ''
updated: 1644061890542
created: 1644061302013
---
Functions are what is called first class citizens. That means that a function can be an arugment of another function and the return value of the function can be a function returning that value. 

## The value of a function can be a function
![](/assets/images/2022-02-05-12-44-55.png)

## The argument of a function can be a function
![](/assets/images/2022-02-05-12-45-38.png)

## Declaration of higher-order functions
Higher order functions as i understand it is where you can have a function that takes in a parameter and parses this to another function. However, the function that this parameter gets parsed on to also contains another parameter. Therefore when calling the "above" method then it also has parameters from the other functions that it contains.

Just like in the example below:
![](/assets/images/2022-02-05-12-51-07.png)
![](/assets/images/2022-02-05-12-51-23.png)