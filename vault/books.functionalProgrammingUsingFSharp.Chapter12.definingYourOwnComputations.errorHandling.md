---
id: s9u35jgqa930rr5nmhuwk1m
title: Error Handling
desc: ''
updated: 1646558340212
created: 1646556927831
---
When trying to handle computaition expression evaluations then most of them can be handled with the `option<'a>` type. 
However, we can also create a computation type `maybe<'a>`. Such a type can be declared like the following:
```F#
type maybe<'a> = option<'a>
```

Here the `None` will denote an error situation and the `Some v` is the conatiner that contains the value $v$.

We create a builder class like this:

![](/assets/images/2022-03-06-10-10-38.png)
![](/assets/images/2022-03-06-10-13-53.png)


## Implementation of the MaybeClass
![](/assets/images/2022-03-06-10-17-46.png)

### Use of the Maybe Class
![](/assets/images/2022-03-06-10-18-16.png)
![](/assets/images/2022-03-06-10-18-54.png)