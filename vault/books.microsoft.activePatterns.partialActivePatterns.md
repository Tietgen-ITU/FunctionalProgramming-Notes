---
id: oesby3aq2r5iruizpyx8qx0
title: Partial Active Patterns
desc: ''
updated: 1647542296269
created: 1647542142571
---
There are some cases where you only partition a part of the input space. In other words *Active Patterns* that do not always produce a value are called *Partial Active Patterns*.

This can be showed by an example:
```F#
let (|Integer|_|) (str: string) =
   let mutable intvalue = 0
   if System.Int32.TryParse(str, &intvalue) then Some(intvalue)
   else None

let (|Float|_|) (str: string) =
   let mutable floatvalue = 0.0
   if System.Double.TryParse(str, &floatvalue) then Some(floatvalue)
   else None

let parseNumeric str =
   match str with
     | Integer i -> printfn "%d : Integer" i
     | Float f -> printfn "%f : Floating point" f
     | _ -> printfn "%s : Not matched." str

parseNumeric "1.1"
parseNumeric "0"
parseNumeric "0.0"
parseNumeric "10"
parseNumeric "Something else"

> 1.100000 : Floating point
> 0 : Integer
> 0.000000 : Floating point
> 10 : Integer
> Something else : Not matched.
```
