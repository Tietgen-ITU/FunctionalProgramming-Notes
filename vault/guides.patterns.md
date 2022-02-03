---
id: PNR6nJvOApCRGUZXfAMrH
title: Patterns
desc: ''
updated: 1643920192647
created: 1643910863864
---
This is notes about everything regarding patterns and pattern matching.

## Functions with pattern matching
In F# you can declare functions which have pattern matching. 
[[books.functionalProgrammingUsingFSharp.Chapter1.functionsExpressionsWithPatterns]]

## Patterns with pairs
In F# you can declare new variables by patterns. [[Pairs variable pattern|books.functionalProgrammingUsingFSharp.Chapter1.pairs#patterns]]

## Order of patterns
It is important to note that the order of the patterns is not random. A general rule is to have the most specific rules at the top and the more general og abstract expressions at the bottom. 
A great example can be seen described [[here|books.functionalProgrammingUsingFSharp.Chapter1.pairs#patterns]].