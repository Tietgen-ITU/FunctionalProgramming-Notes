---
id: qlc1nbipe5cbp9eb4l1v18u
title: Asynchronous Programming
desc: ''
updated: 1649225752486
created: 1649225752486
---
So how do we do asynchronous programming?
We do it by using the `Async<T>` type.

![](/assets/images/2022-04-06-08-16-49.png)

> **Note**: the type 'T' indicates the return type. And not that there is a possibility to have a computational expression.

![](/assets/images/2022-04-06-08-21-38.png)

![](/assets/images/2022-04-06-08-21-54.png)

![](/assets/images/2022-04-06-08-23-47.png)

Now we have seen how to construct a async method. Now we want to start the computation.

![](/assets/images/2022-04-06-08-42-20.png)

#### Exceptions and Cancellations
![](/assets/images/2022-04-06-08-43-25.png)

![](/assets/images/2022-04-06-08-46-20.png)

We can react to cancellation and exceptions and handle it. We can do so with continuation functions.

![](/assets/images/2022-04-06-08-47-51.png)

![](/assets/images/2022-04-06-08-48-36.png)

# Summary
![](/assets/images/2022-04-06-08-49-09.png)