---
id: vhF9srMuNraXuViWxbSwF
title: Records
desc: ''
updated: 1644255246978
created: 1644236984073
---
A records is a generalized [[tuple|books.functionalProgrammingUsingFSharp.Chapter3.tuples]]. However each component in the tuple is identified by a label instead of the position in the tuple. 

A record can be declared like the following example:
```F#
type Person = {age : int; birthday : int * int; name : string; sex : string; };;
```
>**Note:** That the seperation between each component in the record is seperated by the character ';'

In order to create an instance of the record the following can be done:

![](/assets/images/2022-02-07-13-34-23.png)