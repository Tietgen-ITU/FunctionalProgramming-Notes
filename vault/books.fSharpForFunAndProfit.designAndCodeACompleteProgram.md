---
id: a92741mmadldlyqww9o0gkh
title: 1. Design and Code a Complete Program
desc: ''
updated: 1646560975944
created: 1646559458476
---
What we are trying to build here is an application that updates some customer information via a web service.
The following requirements:

![](/assets/images/2022-03-06-10-40-38.png)

When coding we want to not only cover the happy path but also the cases where errors can occur:

![](/assets/images/2022-03-06-10-41-39.png) ![](/assets/images/2022-03-06-10-41-47.png)


# Thinking functionally 
We typically think input/output when programming a request and the response. If there is an error then flow is terminated and a response is returned early.

![](/assets/images/2022-03-06-10-46-17.png)

However when we think functionally, then a function is a black box:

![](/assets/images/2022-03-06-10-46-53.png)


## Functions should be forward only
Functions should be forward only. And what does that mean? You cannot do a "u-turn" or return early. All returns, even errors, should be an alternative path than the happy path.

![](/assets/images/2022-03-06-10-49-06.png)

When this is done then we can convert it to the traditional black box functional thinking: 

![](/assets/images/2022-03-06-10-51-47.png)

But if you of course look into the function then smaller functions or steps is doing all the work in the black box function:

![](/assets/images/2022-03-06-10-54-13.png)

# Summary and Guidelines
![](/assets/images/2022-03-06-11-02-51.png)
