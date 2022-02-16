---
id: RiTzoUyZvbT5RPJBOxfQu
title: Binary Tree
desc: ''
updated: 1644999413305
created: 1644756302334
---
A binary search treee is a tree data structure where a node can have two children. The child on the left of the node is smaller than the current and the child node on the right is larger than the parent node:

![](/assets/images/2022-02-16-08-35-23.png)

# How to create a binary search tree in F#
In order to create a binary tree that looks like the following:

![](/assets/images/2022-02-13-13-45-36.png)

We then first declare a type that represents the tree:
```F#
type BinTree<'a, 'b> = 
    | Leaf of 'a
    | Node of BinTree<'a, 'b> * 'b * BinTree<'a, 'b>;;
```

Here we have created a binary tree that stores some value in the `Leaf` and some other value in the `Node` declare with the polymorphic or generic types `'a` and `'b`[^1].

We create the tree like:

![](/assets/images/2022-02-13-13-50-46.png)

## Pattern matching
We can again do pattern matching like the following:

![](/assets/images/2022-02-13-13-52-37.png)

Here we explore the depth of the tree and uses the `Max` function to find out which of the two sides of the has the deepest length.

## Traversal
In order to traverse the binary tree we can do something similar to the pattern matching.

There is 3 kinds of traversals:
- **Pre-order**: First visit the root node, then we traverse the left subtree in pre-order and finally the right sub-tree in pre-order
- **In-order**: First traverese the left sub-tree in in-order, then visit the root node and traverse the right sub-tree.
- **Post-order**: First traverse the left sub-tree in post-order, then traveres the right sub-tree in post-order and finally visit the root node.

### Example
In order to illustrate this. Here are the functions that traverses down the tree:

![](/assets/images/2022-02-13-14-03-29.png)

We want to traverse down the following tree:

![](/assets/images/2022-02-13-14-04-22.png)

The result is the following:

![](/assets/images/2022-02-13-14-04-45.png)

#### Check for duplicates in the binary tree
```F#
let duplicates bt = 
    let rec aux seen bt = 
        match bt with 
        | Leaf                                         -> (false, seen)
        | Node (_, x, _) when List.exists ((=) x) seen -> (true, seen)
        | Node (l, x, r)                               -> match aux (x::seen) 1 with
                                                          | (true, seen') -> (true, seen')
                                                          | (false, seen*) -> aux seen' r
```
>**Note:** that the `seen'` is not the same as the `seen` variable. Because the other name contains a `'` in the name.

---
[^1] [[books.functionalProgrammingUsingFSharp.Chapter3.polymorphism]]