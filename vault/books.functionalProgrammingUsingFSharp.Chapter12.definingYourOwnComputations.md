---
id: lcpyxkf8edefhmrcpqdulw9
title: Defining Your Own Computations
desc: ''
updated: 1646558754044
created: 1646553847582
---
There are 3 parts when you want to define your own computation:

![](/assets/images/2022-03-06-09-04-49.png)

This could look like the following:
```F#
type comp<’a> = ...
...
type CompBuilderClass() =
    t.Bind(c: comp<’a>, f: ’a->comp<’b>): comp<’b> = ... 
    t.Return(x: ’a): comp<’a> = ...
...
let comp = CompBuilderClass()
```

# Comp<'a>
This is a type that is sort of a recipe in a cook book. 
What it does is that it captures pieces of a program and only executes it if the computation is started. 

Here is how you evaluate a computation:
```F#
let c = comp { ... }
```

Each kind of computation has its own means to start a computation:

![](/assets/images/2022-03-06-09-10-47.png)

# Technical setting on how to define your own computations
Before we go further then I will explain a bit what the different symbols mean:
- $ce$, $ce_1$, and $ce_2$ is computation expressions, which occurs inside the brackets in an expression `comp { ... }`
- $e$ is an computation expression. So it is like `comp { ce }`
- $pat$ is a pattern

#### Usual types of memeber functions
![](/assets/images/2022-03-06-09-54-33.png)

# Controlling the computations: Delay and Start
You can delay the computation of a functionby using the `Delay: (unit -> comp<'a>) -> comp<'a>` function to wrap around the computation.
The use of this function is like the following:

![](/assets/images/2022-03-06-10-25-16.png)