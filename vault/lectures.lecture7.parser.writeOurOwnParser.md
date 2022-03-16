---
id: g71ft802i6uldqmowfvty5f
title: Write our Own Parser
desc: ''
updated: 1647419199249
created: 1647416968076
---
This is about how to use the [[books.fSharpForFunAndProfit.parserCombinators]]. 

We want to define a parser for arithmetic expressions:

![](/assets/images/2022-03-16-08-51-04.png)

![](/assets/images/2022-03-16-08-52-55.png)

![](/assets/images/2022-03-16-08-53-35.png)

![](/assets/images/2022-03-16-08-53-49.png)

#### Parsing negation
![](/assets/images/2022-03-16-08-57-04.png)

#### Parsing something in between
![](/assets/images/2022-03-16-09-02-09.png)

>**Note:** the between parser parses the everything between two parsers. See the top of the picture more closely for an example

#### Parse two things and get a result
![](/assets/images/2022-03-16-09-04-51.png)


#### Result of parsers for our grammar
![](/assets/images/2022-03-16-09-05-30.png)

# How do we parse non-terminals?
![](/assets/images/2022-03-16-09-07-47.png)
>**Note:** The infix means 'or'

However this recursive definition is not accepted in in F#. We are trying to define the function `pT` by calling `pT` without knowing what it is:

![](/assets/images/2022-03-16-09-10-18.png)

So we should try to fix that:

![](/assets/images/2022-03-16-09-10-52.png)

Here we try to fix it by creating a dummy parser so that we can define what it is we want to parse later on.

![](/assets/images/2022-03-16-09-12-45.png)

## Improvements
![](/assets/images/2022-03-16-09-13-55.png)

Also we want to add error messages:

![](/assets/images/2022-03-16-09-15-13.png)

# Summary
![](/assets/images/2022-03-16-09-14-10.png)