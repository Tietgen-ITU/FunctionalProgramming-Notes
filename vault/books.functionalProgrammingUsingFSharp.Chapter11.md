---
id: g4bdhr2y4lgxhxpenp4rdlu
title: 11. Chapter - Sequences
desc: 'This chapter is about sequences. A possibly infinite ordered collection of elements'
updated: 1647540723468
created: 1647535200748
---
Before we start! It is important to state what a sequence is. A sequence is a lot like an `IEnumerable<T>` that we know and love from C#. A sequence in F# is only computed when you ask for it. The type is represented as the following:

```F#
seq<'a>
```

We can create sequences like the following:

```F#
seq [10; 7; -25]
> val it : seq<int> = [10; 7; -25]
```

It is also possible to just compute a specific element in the sequence. You can do so by typing the following:
```F#
let nat = Seq.initInfinite (fun i -> i);;
> val nat : seq<int>

Seq.nth 5 nat;;
> val it : int = 5
```

>**Note:** that the `Seq.initInfinite` function initialize an infinite sequence with the function provided.

# Cached Sequences
A *cached sequence* can be used if a re-computation of elements is undesirable. In other words a cached sequence remembers the initial part of the sequence that has already been computed. 

You can create a cached sequence as the following:
```F#
// Inits a inifinite sequence by using the cache sequence and uses the natWithPrint function to print numbers
let natWithPrintCached = Seq.cache natWithPrint;;
> val natWithPrintCached : seq<int>

// Then we want to print the first 3 elements
Seq.nth 3 natWithPrintCached;;
>  0
>  1
>  2
>  3

// Now we want to print the first 5 elements
Seq.nth 5 natWithPrintCached;;
>  4
>  5
```
>**Note:** Did you see what happened there? The cache has already computed the first 3 elements and therefor when called again it then starts from 4

# Functions for sequences
![](/assets/images/2022-03-17-19-11-10.png)
