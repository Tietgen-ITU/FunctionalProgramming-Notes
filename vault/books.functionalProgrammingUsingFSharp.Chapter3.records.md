---
id: vhF9srMuNraXuViWxbSwF
title: Records
desc: ''
updated: 1644393951964
created: 1644236984073
---
A record is a generalized [[tuple|books.functionalProgrammingUsingFSharp.Chapter3.tuples]]. However each component in the tuple is identified by a label instead of the position in the tuple. 

It allows us to structure data. 

A record can be declared like the following example:
```F#
type Person = {age : int; birthday : int * int; name : string; sex : string; };;
```
>**Note:** That the seperation between each component in the record is seperated by the character ';'

They are declared by providing input to all of their fields. 
In order to create an instance of the record the following can be done:

![](/assets/images/2022-02-09-09-03-44.png)

# Compound statments
It is also possible to create it with compound statements:
![](/assets/images/2022-02-09-09-05-47.png)
