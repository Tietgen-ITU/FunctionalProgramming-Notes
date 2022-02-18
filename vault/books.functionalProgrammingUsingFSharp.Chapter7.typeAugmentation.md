---
id: nqeqTGvqtYuE89cDDJl2k
title: Type Augmentation
desc: ''
updated: 1645126921944
created: 1645124999139
---
Type augmentation adds declarations to the definition of a tagged type or a record type and it allows declaration of operators. 

This has an Object Oriented kind of syntax. 

Look at the following example:

![](/assets/images/2022-02-17-20-12-56.png)
![](/assets/images/2022-02-17-20-13-06.png)

The `member` keyword lets the function become a part of the specified type. So in order to use the function for a specific type then you have to call it by the instance of the type:
```F#
type Vector = float * float
    member SomeFunctions = // some code here...

let a = Vector (2.0, 1.0)

let b = a.SomeFunction
```

>**Note:** that the function has the first letter as upper case.
