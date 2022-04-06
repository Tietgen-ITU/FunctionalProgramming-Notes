---
id: l313ecgxtw1n6823fcivh9r
title: Message-based Synchronisation
desc: ''
updated: 1649228422723
created: 1649228422723
---
So the problems with parallelism and asynchronous computations is that you can have race conditions. And when you want to prevent race conditions then you can have deadlocks. 

This is what this section is about.

![](/assets/images/2022-04-06-09-01-57.png)

# Race Condition
![](/assets/images/2022-04-06-09-02-35.png)

So in order to prevent this we than want to create a lock of the shared resource.

we can do so by using the `lock` function:

![](/assets/images/2022-04-06-09-11-42.png)

# Deadlock
![](/assets/images/2022-04-06-09-27-26.png)

So how do we prevent this? We use a message based approach to handle synchronization.

![](/assets/images/2022-04-06-09-28-17.png)

![](/assets/images/2022-04-06-09-28-44.png)

How do i read from the `MailBoxProcessor`?
You do it by sending a channel to the `MailBoxProcessor`:

![](/assets/images/2022-04-06-09-35-21.png)

![](/assets/images/2022-04-06-09-41-27.png)

# Summary
![](/assets/images/2022-04-06-09-44-08.png)