---
id: etn6migloy98d2p9y32m8de
title: Building Useful Set of Parser Combinators
desc: ''
updated: 1647420668301
created: 1646857191031
---
So we are trying now to go from a parser that returns `(('1', '2'), '3')` i.e. a tuple inside a tuple to a tuple with accumulated string `("12", "3")`.

![](/assets/images/2022-03-16-08-44-01.png)

So this is what we are going to use in the following assignments:

![](/assets/images/2022-03-16-08-45-32.png)

So what we want is to write parser that produces the following type, which indicates that it returns a parser that parses to the datatype defined in the polymorphic type:

![](/assets/images/2022-03-16-08-48-51.png)

![](/assets/images/2022-03-16-09-28-09.png)

We do so by using a newly defined `mapP` function:

![](/assets/images/2022-03-10-19-20-40.png)

We can use it as the following:

![](/assets/images/2022-03-10-19-21-06.png)

![](/assets/images/2022-03-10-19-21-14.png)

# Creating functions to the world of parsers
Now we want to create functions that we normally use in the "normal world" to the world of parsers.

![](/assets/images/2022-03-10-19-23-41.png)

![](/assets/images/2022-03-10-19-24-08.png)

These two functions lift functions from the normal world to the parser world.

# Combining Parsers

## Combine two parsers
The infix `.>>.` will try to parse the first part and then the second part of the string will be parsed by the second parser. Here is the implementation of it:

![](/assets/images/2022-03-16-09-32-07.png)

## Maping results
So here we have a parser which first parses the value and then converts the value to something else that we wants it to be:

![](/assets/images/2022-03-16-09-36-29.png)

And we can continue with this, and implement functions that throws away some other values, and only keeps one of the values generated from the parsers:

![](/assets/images/2022-03-16-09-38-41.png)

## Turning a list of parsers to a single parser

We create the following implementation:

![](/assets/images/2022-03-10-19-27-15.png)

Now we can to the following:

![](/assets/images/2022-03-10-19-28-05.png)

## Matching a parser multiple times
Now we want to be able to run the same parser more than one time.

We create the following function:

![](/assets/images/2022-03-10-19-30-29.png)

And use it as the following:

![](/assets/images/2022-03-10-19-31-07.png)

![](/assets/images/2022-03-10-19-31-22.png)

This is the same thing as using the repeat function from the lecture:

![](/assets/images/2022-03-16-09-42-03.png)

It recursively calls the parser until it fails.

### 1 or more times parser
Here we try to parse the value atleast one time:

![](/assets/images/2022-03-16-09-43-04.png)


### Zero or one time
Now we want to be able to either skip the char or parse it one time:

![](/assets/images/2022-03-10-19-32-55.png)

# Implementing parse to types 

#### pChar parser
We first try to implement `pChar` parser:

![](/assets/images/2022-03-16-09-29-31.png)

Now we wnat to generalize:
![](/assets/images/2022-03-16-09-44-44.png)

We do so by using the `satisfy` function.

# Refining the parser type
![](/assets/images/2022-03-16-09-46-31.png)

So what we want is to implement somekind of state, to symbolize the cursor in the input.

So now we can also give better error messages because of the better information:

![](/assets/images/2022-03-16-09-48-43.png)

![](/assets/images/2022-03-16-09-49-18.png)


# Functions implemented
![](/assets/images/2022-03-10-19-33-43.png)

# Summary
![](/assets/images/2022-03-16-09-51-05.png)