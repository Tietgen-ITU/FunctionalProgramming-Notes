---
id: xCz7b8y2bLUhF60iM7kjL
title: Tagged Values
desc: ''
updated: 1644256835973
created: 1644255417311
---
Tagged values are used when we group together values of different kinds to form a single set of values. 

For example we have the following values representing a specific type:

![](/assets/images/2022-02-07-18-39-42.png)

In F# tagged values is being declared like the following:

![](/assets/images/2022-02-07-18-40-15.png)

# Constructor
![](/assets/images/2022-02-07-18-41-43.png)

# Constructors in patterns
![](/assets/images/2022-02-07-18-42-38.png)

Constructors can be used in patterns. 
In order to do so we make a pattern matching for each type that we want to which has been declared as a tagged value and create the way that it should be initialized.
Just like the example below:
![](/assets/images/2022-02-07-18-49-11.png)

The way that method is being called is like the following:
```F#
let square : Shape = area(Square 2);;

let circle : Shape = area(Circle 5);;

let triangle : Shape = area(Triangle 5 5 4);;
```

>**Note:** See that the type which is being returned of from the `area()` function is a type of `Shape`. This is because the types in the pattern mathcing has the same "parent value".

## Invariant for the representation of shapes
Sometimes the value which is being provided is not correct. If we take the shape example then a circle with -1 in radius is not a circle.

For that reason we need to check that the values are correct be for "instanciating" the type with that specific value. 

For this particular example, an `isShape` function is being created with pattern matching. Here it is taking the value to see if it is correct. In other words it is defining a set of rules for that particular shape:

![](/assets/images/2022-02-07-18-57-32.png)

We now add that function to the `area()` function before:

![](/assets/images/2022-02-07-18-58-43.png)
>**Note:** That it has a if and else clause. Here it is throwing an exception if the function does not declare it a shape. Also note the alternativ pattern expression with the `match` keyword.
