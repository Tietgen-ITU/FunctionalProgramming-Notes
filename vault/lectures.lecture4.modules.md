---
id: SKukNsj8A5u0HZSYm4reg
title: Modules
desc: ''
updated: 1645602407555
created: 1645600361655
---
A lot of what is covered here is also in the [[books.functionalProgrammingUsingFSharp.Chapter7.signatureAndImplemention]].

Modular programming design 
- Encapsulation
- Abstraction
- Reuse of components

A module is characterised by 
- A signature file (.fsi)
- A matching implementation (.fs)

# Signatures
![](/assets/images/2022-02-23-08-15-20.png)

What to note here is that the implementation detail is not given in fsi file. So we do not define what the `T` type is.

![](/assets/images/2022-02-23-08-18-15.png)

![](/assets/images/2022-02-23-08-18-30.png)

## Example in lecture

#### Definition
![](/assets/images/2022-02-23-08-38-12.png)

#### Implementation
![](/assets/images/2022-02-23-08-38-31.png)

This sadly gives us a typing error:

![](/assets/images/2022-02-23-08-38-57.png)

These are the following solutions that we have:

![](/assets/images/2022-02-23-08-39-27.png)

We can instead do the following if we want to keep the signature:

![](/assets/images/2022-02-23-08-40-15.png)

#### Implementation
![](/assets/images/2022-02-23-08-40-45.png)

#### Result
![](/assets/images/2022-02-23-08-41-10.png)

# Override
![](/assets/images/2022-02-23-08-45-43.png)

>**Note:** see that `q` is in the method. Just see this at to apply this method