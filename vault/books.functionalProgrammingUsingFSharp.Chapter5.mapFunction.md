---
id: K6npxYqoRhnT676NeAoXN
title: List Map Function
desc: 'Describes the List.map function'
updated: 1644395789058
created: 1644300610157
---
The `List.map` function is a function associated to the `List`(See section [[books.functionalProgrammingUsingFSharp.Chapter4.list]]).

The map function applies a function $f$ to each element in a list.
A list map use case could be to add the `".fs"` file extension to every string in the list:
![](/assets/images/2022-02-08-07-13-35.png)

The `List.map`function returns what is called a beta list:
```F#
map : ('a -> 'b) -> 'a list -> 'b list
```

Here is the implementation of the function:
![](/assets/images/2022-02-09-09-27-56.png)

## Example of use
![](/assets/images/2022-02-09-09-29-53.png)
>**Note:** that the last example has removed the lst variable becuase the `List.map` requires it. So implicit this is requried if not provided. This is covered in the [[books.functionalProgrammingUsingFSharp.Chapter2.higherOrderFunctions]].

# Evaluation
This seems complicated but essentially what it does is running the map function with the add function. A quick tip before you look at the below example follow the arrows and look at the difference:

![](/assets/images/2022-02-09-09-32-22.png)