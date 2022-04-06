---
id: zvp09e6udtnw4dgliq6t8iq
title: Regex
desc: ''
updated: 1647534416362
created: 1647533701817
---
Regex, or *regular expressions* as they are also called, are expressions that takes somekind of pattern into account. 
In order to use them in F# then we have the following:

![](./assets/images/2022-03-17-17-16-31.png)

Here are also a list of functions that can be used to either just parse one or more types of the regex provided:

![](/assets/images/2022-03-17-17-19-57.png)


# Parsing nested data
Here is an example from the book of parsing nested data that can be useful. This is what it is trying to parse:

![](/assets/images/2022-03-17-17-23-49.png)

In order to do so a regular expression is needed:

![](/assets/images/2022-03-17-17-24-24.png)

This is the result of the parsing:

![](/assets/images/2022-03-17-17-24-45.png)

However, it is better to parse using a [[lectures.lecture7.parser]] that is monadic. 

## Lecture
This is the way we did it in the lecture:

![](/assets/images/2022-03-23-08-27-13.png)