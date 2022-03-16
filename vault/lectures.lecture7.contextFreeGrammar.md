---
id: apft4segx7ilclyuttdz90n
title: Context Free Grammar
desc: ''
updated: 1647415944142
created: 1647414259590
---
![](/assets/images/2022-03-16-08-04-46.png)

![](/assets/images/2022-03-16-08-05-04.png)

Here is an example of a context free grammar, with the short hand definition of grammar:

![](/assets/images/2022-03-16-08-06-09.png)

This is what we have known from discrete math:

![](/assets/images/2022-03-16-08-07-48.png)

#### Terminal Symbols
![](/assets/images/2022-03-16-08-08-05.png)

#### Non-terminal symbols
![](/assets/images/2022-03-16-08-08-28.png)


# Syntax tree
![](/assets/images/2022-03-16-08-12-31.png)

And that is what we want our data in. But when we get data then we do not have structured input every time. For that reason we need a parser:

![](/assets/images/2022-03-16-08-13-31.png)

So in other words we want to go from unstructured data to structured data.

# Left recursive grammars to right recursive
We can have difficulties by parsing left to right. That is becuase we have to look ahead, in order to determine which rule we want to use:

![](/assets/images/2022-03-16-08-27-27.png)

![](/assets/images/2022-03-16-08-27-41.png)

So we want to remove the left recursivness:

![](/assets/images/2022-03-16-08-28-17.png)

![](/assets/images/2022-03-16-08-28-52.png)

# Summary
![](/assets/images/2022-03-16-08-30-57.png)