---
id: 8j8obzpbta7wmtvxafdl0hd
title: Lazy Evaluation
desc: ''
updated: 1648021680294
created: 1648021680294
---
What is lazy evaluation? It is where it evaluates the function only when it being used. 

The illustration below is a very good example of it:

![](/assets/images/2022-03-23-08-48-59.png)

F# is not standard *Lazy evaluation* and that is the reason for [[lectures.lecture8.sequences]]. 

![](/assets/images/2022-03-23-08-50-18.png)

# Delayed computation
We can delay computation of expressions by wrapping them into functions: 

![](/assets/images/2022-03-23-08-51-49.png)