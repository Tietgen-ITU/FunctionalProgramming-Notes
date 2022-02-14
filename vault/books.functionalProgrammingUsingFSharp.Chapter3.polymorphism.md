---
id: CdRV6l61Z6fbAdmIUUH1A
title: Polymorphism
desc: ''
updated: 1644758464280
created: 1644236285240
---
A polymorphic function in F# is a function that contains types which is polymorphic. 

A polymorphic type is denoted as `'a` or `'b` etc. 

Polymorhic means "of many forms" and is a way to have a function work on multiple types.

# Type restriction
We can also make type restriction to the generic/polymorphic type with the `:` and `when` keyword.

```F#
'a when 'a : <Type to restrict it to>
```

An example of this is:
![](/assets/images/2022-02-13-14-20-00.png)