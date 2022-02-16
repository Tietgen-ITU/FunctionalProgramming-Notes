---
id: nbIkcX8YuPisWHA3ky3SW
title: Finite Sets
desc: ''
updated: 1644999888577
created: 1644687323351
---
This is notes about the datastructure `Set` in F# and actually mathematics. 
Because this data structure is the exact same behavior of the one we have in discrete mathematics. 

A `Set` is an unordered collection.

![](/assets/images/2022-02-16-09-18-25.png)

# Math basics
To start of a bit light then we denote the most basic things surrounding around a set.


## Subset and equality
To say that a set is a subset of another set then we do the following:

![](/assets/images/2022-02-12-18-39-30.png)

A set is equal if:

![](/assets/images/2022-02-12-18-39-47.png)

## Union, intersect and difference
![](/assets/images/2022-02-12-18-40-34.png)
![](/assets/images/2022-02-12-18-40-40.png)

Here is an example of the set with the applied functions:
![](/assets/images/2022-02-12-18-41-00.png)

# Programming
When you want to create a set you can do it like the following:
```F#
set [3;1;2;4;7;8;1];;
```

Then the following will show in the terminal:
```F#
val it : Set<int> = set [1; 3; 5 ; 7 ; 9]
```
>**Note:** that there is only one '1' in the set. That is because you can only have one value that is the same in a `Set`

## Equality
Equality of two sets is tested in the same way as usual:

![](/assets/images/2022-02-12-18-55-25.png)

You can also compare two sets:

![](/assets/images/2022-02-12-18-55-39.png)

## Operations
![](/assets/images/2022-02-12-18-56-01.png)

Functions from the lecture 3:
![](/assets/images/2022-02-16-09-19-13.png)
## Union, intersect and difference operations
![](/assets/images/2022-02-12-18-57-29.png)

