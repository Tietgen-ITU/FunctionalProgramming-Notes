---
id: mndkgwnfxeniattv29r4uqa
title: Iterative Functions
desc: ''
updated: 1646676572502
created: 1646205978861
---
[[books.functionalProgrammingUsingFSharp.Chapter9.tailRecursionObtainedUsingContinuations]]

What we want to achieve here is the tail recursion. 

We want to avoid of building up the stack. With tail recursion is that you have coded a recursive call but it gets optimized to a iterativ function instead when compiled. 

![](/assets/images/2022-03-02-08-43-09.png)

# Accumulators
![](/assets/images/2022-03-02-08-43-36.png)

The accumulator is a value that gets passed through each recursive call. Notice that we perform a computation before passing it to the next recursive call.

![](/assets/images/2022-03-02-08-49-10.png)

Notice that we do not have to keep "saving" the recursive calls.

This can also be done for the *List reversal* function:

![](/assets/images/2022-03-02-08-57-23.png) 

## Refine the factA function
Now the issue is that you now expose the `acc` to the user of the `factA` function. This can be problematic because the value should not be anything else but 1 to start with. Therefor we can wrap it into another function:

![](/assets/images/2022-03-02-08-55-54.png)

# Continuation functions
![](/assets/images/2022-03-02-09-08-22.png)

![](/assets/images/2022-03-02-09-09-58.png)

Instead we will try to use continuation functions. Sooo...

![](/assets/images/2022-03-02-09-10-51.png)

So the code looks like this now:

![](/assets/images/2022-03-02-09-11-53.png)

So when running the function it looks like this:

![](/assets/images/2022-03-02-09-17-35.png)

## Example
The example that we are going to show now is applied on a binary tree.

![](/assets/images/2022-03-02-09-28-44.png)
![](/assets/images/2022-03-02-09-30-03.png)

Here is the new way using the continuation function:

![](/assets/images/2022-03-02-09-31-16.png)
![](/assets/images/2022-03-02-09-34-34.png)

Here is how it works when it gets called:
![](/assets/images/2022-03-02-09-37-38.png)

>**Note:** That `id` is just a function that returns the value that it gets in as an input.

![](/assets/images/2022-03-02-09-39-05.png)

## Why does continuation work? 
This works because functions are stored on the heap. So by sort of saving the computations as a function it the stores it on the heap. 

![](/assets/images/2022-03-02-09-44-00.png)
