---
id: qxvb3tzs6ihdjl0hoq8uipn
title: Write Regex In F#
desc: ''
updated: 1648019714670
created: 1648019714670
---

![](/assets/images/2022-03-23-08-15-50.png)

![](/assets/images/2022-03-23-08-16-05.png)

We can use capturing groups and use the `TextProcessing` library to do something with it:

![](/assets/images/2022-03-23-08-18-46.png)

![](/assets/images/2022-03-23-08-19-00.png)

# Matches
So we want to get the following matches.
![](/assets/images/2022-03-23-08-22-12.png)


But we can quickly see that some of the things does not get matched!
![](/assets/images/2022-03-23-08-21-20.png)

![](/assets/images/2022-03-23-08-21-27.png)

We can fix it with the following:

![](/assets/images/2022-03-23-08-23-29.png)

# Capturing nested data
[[books.functionalProgrammingUsingFSharp.Chapter10.regex#parsing-nested-data]]
