---
id: OQvZyTwAYNs64KOtYKpRF
title: Exceptions
desc: ''
updated: 1644257675287
created: 1644256933992
---

In order to throw an exception you can use the keyword `failwith`.
This can be used as the following example

![](/assets/images/2022-02-07-19-07-04.png)

```F#
failwith <string value declaring a message>
```

This throws an exception with the type `Failure`.

However it is also possible to use the `raise` keyword to throw an exception.
Here you declare what kind of "type" it should throw. 

We can use that later when catching the exceptions.

For now look at this example on how to raise a custom exception:
![](/assets/images/2022-02-07-19-11-36.png)

# Catch exceptions
When catching exceptions we use `try ... with ...` keyword.
An example of that is the following:

![](/assets/images/2022-02-07-19-12-34.png)

The pattern of declaring try with is like this:
```F#
try 
    // Some code
with    
    // Some match code
```

The match code can be like the regular pattern matching code. An example of how to do so is like the first picture in this section.
