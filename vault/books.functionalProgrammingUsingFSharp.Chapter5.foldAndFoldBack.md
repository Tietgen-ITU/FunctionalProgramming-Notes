---
id: 3ScHvVzpllt1tgoB0jN8E
title: Fold And FoldBack
desc: ''
updated: 1644396548047
created: 1644301018456
---
## Fold
The `List.fold` function is when you want to perform a calculation on a list. The `List.fold`function is like the [[books.functionalProgrammingUsingFSharp.Chapter5.mapFunction]] in that it performs the function on each element in the list. However, the difference is that the `List.fold`carries over what is called the *accumulater*. The *accumulater* is some data/value that can be carried to each evaluation of the element. 

The *accumulater* is being assigned by the return value of the delegate/anonymous function being provided to the `List.fold`function. 

The `List.fold` takes in the following parameters:
```F#
List.fold <a delegate> <initial value of the accumulater> <the list of values to go through>
```

Look at the following example:
![](/assets/images/2022-02-08-10-24-52.png)
>**Note:** that the `s` is the accumulater value. `vs` is the list of values. And the `fun` keyword denotes the delegate function.

Here is another example of using the fold function with the `::`("cons"):
![](/assets/images/2022-02-08-10-33-54.png)

The `List.fold` function starts from the start i.e. index 0.

## FoldBack
The `List.foldBack` is basically the same as the `List.fold` function. The way that it differs is that the `List.foldBack` starts from the bottom i.e. the last index of the list.

# Evaluation example
![](/assets/images/2022-02-09-09-47-02.png)