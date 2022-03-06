---
id: 8atscnqhncszvfj4w637gir
title: Railway Oriented Programming
desc: ''
updated: 1646562453507
created: 1646561068641
---
Here we will try to define the pipe we saw before with the `Result<'Success, 'Failure>` type. 

We first look at the Validate function. Here the data can be valid or not. The function can be defined as such:

![](/assets/images/2022-03-06-11-09-30.png)

This gives the following signature:

![](/assets/images/2022-03-06-11-09-47.png)

# The Railway
In railway oriented programming we want to connect the paths of success and connect the paths of failures/errors. 

![](/assets/images/2022-03-06-11-11-43.png)

This is a great way of an analogy of railways:

![](/assets/images/2022-03-06-11-12-11.png)

So the function will look like this:

![](/assets/images/2022-03-06-11-12-40.png)

## How do we connect them?
We can use [[lectures.lecture2.functionComposition]] to connect them.

![](/assets/images/2022-03-06-11-14-36.png)

But there is one issue where you only take one thing as an input but the function outputs two different paths. How do we handle that?

![](/assets/images/2022-03-06-11-15-22.png)

### Converting switches to two track inputs
In order to adapt the two functions then we can use an adapter function.

![](/assets/images/2022-03-06-11-17-00.png)

And the implementation of the function looks like this:

![](/assets/images/2022-03-06-11-17-36.png)
![](/assets/images/2022-03-06-11-19-51.png)

Notice that the function takes a normal function and the `Result` type as an input. 
If the result was good then that could be returned. If not then the error will be propagated further through the line.

#### Example of using the two bind function
![](/assets/images/2022-03-06-11-21-16.png)
![](/assets/images/2022-03-06-11-21-23.png)

## Description of all of the functions described to implement railway programming
![](/assets/images/2022-03-06-11-25-26.png)

![](/assets/images/2022-03-06-11-26-12.png)
![](/assets/images/2022-03-06-11-26-25.png)

# Summary
![](/assets/images/2022-03-06-11-26-52.png)
![](/assets/images/2022-03-06-11-27-15.png)
