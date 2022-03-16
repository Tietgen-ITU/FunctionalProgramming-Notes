---
id: x03nf87l6i9yr7hp6yi1iz8
title: Parser Combinators
desc: ''
updated: 1647416619745
created: 1646854718088
---
This is an article about *parser combinators*. You can find the website [here](https://fsharpforfunandprofit.com/series/understanding-parser-combinators/).

# What is parser combinators?
The signature of a parser looks roughly like this. Note that this is preliminary and simplified:

![](/assets/images/2022-03-09-20-42-59.png)

![](/assets/images/2022-03-09-20-43-08.png)

A parser is something that that takes one thing at a time and evalutates it. The above `parseA` figure returns the remaining chars that needs to be parsed and either a true false value if the value previously was parsed. 

We will improve this concept through out the sections

# Add rail way programming 
One of the improvements is that we do not hard code the value that needs to be parsed. 
AND! We now return a `ParsedResult<char * string>`.

So the signature looks like this:

![](/assets/images/2022-03-09-20-50-30.png)

![](/assets/images/2022-03-09-20-50-46.png)

Also he shifts the parser function `pChar` to be curried([[guides.currying]]). 

![](/assets/images/2022-03-09-20-52-35.png)

![](/assets/images/2022-03-09-20-52-43.png)

What is the benefit of currying? It is that we can now partially apply the functions. So now we can specify that a specific function only parses the char 'A':

![](/assets/images/2022-03-09-20-56-24.png)

In that way we can resuse the function.

# Encapsulating the parsing function in a type
Now we want to hide the function that parses the string. We do so by declaring a type:

![](/assets/images/2022-03-09-20-59-03.png)

![](/assets/images/2022-03-09-20-59-10.png)

![](/assets/images/2022-03-09-20-59-30.png)

So instead of returning the function we then return the type(which hides the details).

#### What is the benefits of this?
![](/assets/images/2022-03-09-21-00-18.png)

## How do we use it?
Now in order to call and use the type we can do the following:

![](/assets/images/2022-03-09-21-02-57.png)

# Combining parsers
Now is where we try to build the framework. We need to first create the function that combines them. In here we use [[lectures.lecture2.functionComposition]]. 

![](/assets/images/2022-03-09-21-10-42.png)

But we can extend this even further:

![](/assets/images/2022-03-09-21-11-03.png)

![](/assets/images/2022-03-09-21-11-11.png)

## Choosing between two parsers
Now we want to implment a sor of if else parser logic.
In this example they create an `orElse` function:

![](/assets/images/2022-03-09-21-12-45.png)

![](/assets/images/2022-03-09-21-12-59.png)

## Choosing from a list of parsers
Now we want to have a list of parser to choose from. We do so by creating the following function:

![](/assets/images/2022-03-09-21-14-53.png)

We here after create a function to create the parser with a list of chars:

![](/assets/images/2022-03-09-21-16-15.png)
