---
id: gi8ofop0nj9l8v4yixz09q6
title: Parser
desc: ''
updated: 1647415470816
created: 1647414855372
---
In short terms this is a parser:

![](/assets/images/2022-03-16-08-14-26.png)

So we define a grammar in order to convert the two things into something that we understand. We want to define some rules in order to know what the input is "like":

![](/assets/images/2022-03-16-08-14-52.png)

# Precedence
It is important to be aware of precedence. e.g.

![](/assets/images/2022-03-16-08-19-37.png)

So for this reason we change our grammar:

![](/assets/images/2022-03-16-08-20-01.png)

So it will now parse it correctly:

![](/assets/images/2022-03-16-08-20-36.png)