---
id: trypa7tfbex3uxmflek2fk3
title: Organizing Modules In a Project
desc: ''
updated: 1646565949135
created: 1646562479784
---
In order to design an application in F# we then think in layers:

![](/assets/images/2022-03-06-12-05-32.png)
>**Note:** Arrows denotes the dependencies between the layers

In order to make it maintainable we need to both define data types and logic. For that reason each layer gets the following definition:

![](/assets/images/2022-03-06-12-06-54.png)

The book explains the two subtypes of layers as the following:
- Data types: Data strucures that are used by that layer
- Logic: Functions that are implemented in that layer

Notice that there was a back reference(the read arrow). In functional programming we move the dependency further down the list:

![](/assets/images/2022-03-06-12-10-34.png)

#### Translating layers to files
Now we can translate these layers to files where we can put in our code. When doing so then we need to be aware of these bullet points:

![](/assets/images/2022-03-06-12-13-24.png)

The project with files could look like this:

![](/assets/images/2022-03-06-12-13-56.png)

The code in the *UseCases.fs* is where all the modules are glued together into a single function that represents a particular use case or service request. 

# Structuring Modules
In F# we do not structure code in classes instead we use [[lectures.lecture4.modules]]. 

There are 3 differnet patterns for mixing types and fucntions together:

![](/assets/images/2022-03-06-12-19-24.png)

### Module approaches

#### 1. Example
![](/assets/images/2022-03-06-12-20-03.png)

#### 2. Example
![](/assets/images/2022-03-06-12-20-18.png)

#### 3. Example
![](/assets/images/2022-03-06-12-20-36.png)
>**Note:** The `AutoOpen` attribute makes the types and functions defined in the module globally available. The module is open in every code file in the project. 

## Organizing modules
When trying to structure the modules then the following guidelines can be applied:

If a type is shared among multiple modules then put it in a special *types-only* module:

![](/assets/images/2022-03-06-12-24-57.png)

If a type is private to a module then put it in the same module as its related functions:

![](/assets/images/2022-03-06-12-25-39.png)