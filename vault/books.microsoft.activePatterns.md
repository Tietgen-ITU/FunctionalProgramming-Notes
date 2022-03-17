---
id: y9kesylgakde2thdh36vxf4
title: Active Patterns
desc: ''
updated: 1647542461255
created: 1647541618973
---
Here we are going to take notes about active patterns.
You can find the page about it [here](https://docs.microsoft.com/en-us/dotnet/fsharp/language-reference/active-patterns).

According to microsoft then Active patterns do the following:
>"Active patterns enable you to define named partitions that subdivide input data, so that you can use these names in a pattern matching expression just as you would for a discriminated union. You can use active patterns to decompose data in a customized manner for each partition." - Microsoft

So in other words you can create somekind of function that lets you define whether the data that comes in is one of the following patterns. 

The documentation about it looks like this:
```F#
// Active pattern of one choice.
let (|identifier|) [arguments] valueToMatch = expression

// Active Pattern with multiple choices.
// Uses a FSharp.Core.Choice<_,...,_> based on the number of case names. In F#, the limitation n <= 7 applies.
let (|identifier1|identifier2|...|) valueToMatch = expression

// Partial active pattern definition.
// Uses a FSharp.Core.option<_> to represent if the type is satisfied at the call site.
let (|identifier|_|) [arguments] valueToMatch = expression
```

So in other words you can create the following function in order to determine if an integer is either Odd or Even:
```F#
let (|Even|Odd|) input = if input % 2 = 0 then Even else Odd

// Example of use
let TestNumber input =
   match input with
   | Even -> printfn "%d is even" input
   | Odd -> printfn "%d is odd" input

TestNumber 7
> 7 is odd

TestNumber 11
> 11 is odd

TestNumber 32
> 32 is even
```

