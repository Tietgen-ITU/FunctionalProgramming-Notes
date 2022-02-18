---
id: 6u6R9qLpxV3lUGKWKRFvZ
title: Signature & Implemention
desc: ''
updated: 1645124979824
created: 1645123701952
---
There are two files at the compilation of a C# module.
- Signature File
- The file that implements the details specified by a particular *signature file*. We define it as the implementation file from now on.

If the implementation file tries to implement a signature file then it must implement the details exactly. 

# Example
Here is the signature file:

![](/assets/images/2022-02-17-19-55-37.png)

#### The implementation of the `Vector` module
![](/assets/images/2022-02-17-19-56-07.png)
>**Note:** that the `type Vector` does not have a signature. It does not need that because you can let the implementor to take care of does details.

When we want to use the module then we do as the following:
![](/assets/images/2022-02-17-19-57-15.png)
>**Note:** the use of `open` keyword. This keyword needs to be declared in order to open up the module. 

It is possible to open module by the `open` keyword. However it is also possible to use the functions without opening the module. You can do so with the following line:

```F#
<Name of the module>.<function name>;;

Vector.make(1.0, -2.0);;
```

# Composite Naming of modules
You can name a module like we did before however we can also extend the name with more meaning by seperating each Word of the namespace by a `.`. This could look like:

```F#
module MyLibrary.Vector

// We open the module by...
open MyLibrary.Vector;;
let a = make(1.0, -2.0);;

// Or...
open MyLibrary;;
let a = Vector.make(1.0, -2.0);;

// And can use functions without opening the module by...
let a = MyLibrary.Vector.make(1.0, -2.0);;
```

# Files and compilation
We have to following file definitions:

![](/assets/images/2022-02-17-20-07-44.png)

We produce a `.dll` file by the following command:

![](/assets/images/2022-02-17-20-09-10.png)

