---
id: u5Bm0WgcVdCa1lUEhKLNw
title: Exception
desc: ''
updated: 1644392465098
created: 1644392375100
---
It is possible to declare your own types of exceptions.
You can do so like the following:
```F#
exception ExceptionName
```

You can raise the exception by using `raise` keyword followed be the name of the exception:
```F#
raise ExceptionName
```
