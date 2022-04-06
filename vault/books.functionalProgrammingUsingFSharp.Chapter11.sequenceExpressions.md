---
id: 6r50nrslo1zvdsrnoip0khe
title: Sequence Expressions
desc: ''
updated: 1647541524879
created: 1647540733323
---
Sequence expressions is a special kind of [[lectures.lecture6.computationExpressions]] that allows us to do a step-by-step generation of sequences. we have seen it before somewhere in the computation expression part of the notes.

This is following that generates the sequence as an expression:
```
seq { seqexp }
```

We have two keywords that are important:
- `yield` which adds the element to the sequence
- `yield!` which adds a sequence to another sequence

![](/assets/images/2022-03-17-19-23-58.png)

Here we have the different constructs for the sequence expressions:

![](/assets/images/2022-03-17-19-24-30.png)

An example of *Sequences* that is constructed with Expressions is implicitly lazy. In other words the `Seq.delay` function is wrapped around the sequence:

![](/assets/images/2022-03-23-09-46-47.png)

# Translations of expression keywords
![](/assets/images/2022-03-23-09-47-22.png)

![](/assets/images/2022-03-23-09-47-39.png)

![](/assets/images/2022-03-23-09-48-41.png)