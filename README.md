# useful-functions-in-languages
A list of builtIn functions in C#, Javascript and Golang

##
Math
---

Js
```
let a = Math.abs(-4.7) // a = 4.7

let a = Math.ceil(0.60) // a = 1
let b = Math.ceil(0.10); // b = 1
let c = Math.ceil(-5.9); // c = -5

let a = Math.floor(0.61); // a = 0
let b = Math.floor(0.40); // b = 0
let c = Math.floor(5); // c = 5
let d = Math.floor(5.1); // d = 5


let a = Math.round(2.60); // a = 3
let b = Math.round(2.50); // b = 3
let c = Math.round(2.49); // c = 2
let d = Math.round(-2.60); // d = -3
let e = Math.round(-2.50); // e = -2
let f = Math.round(-2.49); // f = -2
let g = Math.round(-2.51); // f = -3

let a = Math.pow(4,3) // a = 64

let a = Math.max(5, 10); // a = 10
let b = Math.max(5, 10,25,100) // b = 100

let a = Math.min(5, 10); // a = 5
let b = Math.min(1.5, 10,25,100.9) // b = 1.5

let a = Number.MIN_VALUE // a = 5e-324
let b = Number.MAX_VALUE // b = 1.7976931348623157e+308
```

Go
```
import "math"

a := math.Abs(-4.7) // a = 4.7

a := math.Ceil(0.60) // a = 1
b := math.Ceil(0.10); // b = 1
c := math.Ceil(-5.9); // c = -5

a := math.Floor(0.61); // a = 0
b := math.Floor(0.40); // b = 0
c := math.Floor(5); // c = 5
d := math.Floor(5.1); // d = 5


a := math.Round(2.60); // a = 3
b := math.Round(2.50); // b = 3
c := math.Round(2.49); // c = 2
d := math.Round(-2.60); // d = -3
e := math.Round(-2.50); // e = -2
f := math.Round(-2.49); // f = -2
g := math.Round(-2.51); // f = -3

a := math.Pow(4,3) // a = 64

a := math.MaxInt // MaxInt32 or MaxInt64 depending on intSize.
b := math.MinInt // MinInt32 or MinInt64 depending on intSize.
```

C#
```
using System;

var a = Math.Abs(-4.7) // a = 4.7

var a = Math.Ceil(0.60) // a = 1
var b = Math.Ceil(0.10); // b = 1
var c = Math.Ceil(-5.9); // c = -5

var a = Math.Floor(0.61); // a = 0
var b = Math.Floor(0.40); // b = 0
var c = Math.Floor(5); // c = 5
var d = Math.Floor(5.1); // d = 5


var a = Math.Round(2.60); // a = 3
var b = Math.Round(2.50); // b = 3
var c = Math.Round(2.49); // c = 2
var d = Math.Round(-2.60); // d = -3
var e = Math.Round(-2.50); // e = -2
var f = Math.Round(-2.49); // f = -2
var g = Math.Round(-2.51); // f = -3

var a = Math.Pow(4,3) // a = 64

var a = Math.Max(5, 10); // a = 10
var b = Math.Max(5, 10,25,100) // b = 100

var a = Math.Min(5, 10); // a = 5
var b = Math.Min(1.5, 10,25,100.9) // b = 1.5

var a = Int32.MIN_VALUE // a = -2147483648
var b = Int32.MAX_VALUE // b = 2147483647
```

##
Strings
---

Js
```
Length
let text = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"; 
let l = text.length; // l = 26

String Extraction
substring(indexStart) , substring(indexStart, indexEnd)
let a = "ABCDEFGHIJKLMNOPQRSTUVWXYZ".substring(0,1) // a = A
let b = "ABCDEFGHIJKLMNOPQRSTUVWXYZ".substring(0,6) // b = ABCDEF

Contains
let a = "ABCDEFGHIJKLMNOPQRSTUVWXYZ".includes("A") // a = true
let b = "ABCDEFGHIJKLMNOPQRSTUVWXYZ".includes("1") // b = false

Lookup String index
let a = "I think Ruth's dog is cuter than your dog!".indexOf('dog') // a = 15
let b = "I think Ruth's dog is cuter than your dog!".lastIndexOf('dog') // b = 38

Replace
let a = "I think Ruth's dog is cuter than your dog!".replace("dog",'cat') // a = I think Ruth's cat is cuter than your dog!
let b = "I think Ruth's dog is cuter than your dog!".replaceAll("dog",'cat') // b = I think Ruth's cat is cuter than your cat!

Splitting
let a = 'The quick brown fox jumps over the lazy dog.'.split(' ') // a[0] = "The"

Concatenation
let a = "Hello".concat(' ',"Mya") // a = "Hello Mya"

Trimming
let a = '   Hello world!   '.trim() // a = "Hello World"
let b = '   Hello world!   '.trimStart() // b = "Hello world!   "
let c = '   Hello world!   '.trimEnd() // c = "   Hello world!"

Uppercase/Lowercase
let a = 'The quick brown fox jumps over the lazy dog.'.toUpperCase() // a = "THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG."
let b = 'The quick brown fox jumps over the lazy dog.'toLowerCase() // b = "the quick brown fox jumps over the lazy dog."

Repeat
let a = 'Happy! '.repeat(3) // a = Happy! Happy! Happy! 

```


