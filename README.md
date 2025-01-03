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

Go
```
import "strings"
Length
a := len("abc") // a = 3

String Extraction
a := "World!" // a[0:2] = "Wo"

Contains
a := strings.Contains("seafood", "foo") // a = true

Lookup String index
a := strings.Index("chicken", "ken") // a = 4
b := strings.LastIndex("go gopher", "go") // b = 3

Replace
a := strings.Replace("oink oink oink", "k", "ky", 2) // a = oinky oinky oink
b := strings.Replace("oink oink oink", "oink", "moo", -1) // b = moo moo moo
c := strings.ReplaceAll("oink oink oink", "oink", "moo") // c = moo moo moo

Splitting
s := strings.Split("a,b,c", ",") // s = ["a" "b" "c"]

Concatenation
c := "word" + "bible" // c = "Word bible"

Trimming
s : strings.TrimSpace(" \t\n Hello, Gophers \n\t\r\n") // s = Hello, Gophers
x := strings.Trim("¡¡¡Hello, Gophers!!!", "!¡") // x = Hello, Gophers
b := strings.TrimLeft("¡¡¡Hello, Gophers!!!", "!¡") // b = Hello, Gophers!!!
a := strings.TrimRight("¡¡¡Hello, Gophers!!!", "!¡") // a = ¡¡¡Hello, Gophers

Uppercase/Lowercase
d := strings.ToUpper("Gopher") // d = GOPHER
e := strings.ToLower("Gopher") // d = gopher

Repeat
s := strings.Repeat("na", 2) // s = nana
```

C#
```
Length
var text = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"; 
var l = text.Length; // l = 26

String Extraction
Substring(int startIndex,int length)
var a = "ABCDEFGHIJKLMNOPQRSTUVWXYZ".Substring(1,6) // a = BCDEFG
var b = "ABCDEFGHIJKLMNOPQRSTUVWXYZ".Substring(24) // b = YZ

Contains
var a = "ABCDEFGHIJKLMNOPQRSTUVWXYZ".Contains("A") // a = true

Lookup String index
var a = "I think Ruth's dog is cuter than your dog!".IndexOf('d') // a = 15
var b = "I think Ruth's dog is cuter than your dog!".LastIndexOf('d') // b = 38

Replace
var a = "I think Ruth's dog is cuter than your dog!".Replace("d",'c') // a = I think Ruth's cog is cuter than your cog!

Splitting
var a = 'The quick brown fox jumps over the lazy dog.'.Split(' ') // a[0] = "The"

Concatenation
var a = "Hello".Concat(" Mya") // a = "Hello Mya"
var b = string.Join(" ", "Hello", "Hi", "Howdy"); // "Hello,Hi,Howdy"

Trimming
var a = '   Hello world!   '.Trim() // a = "Hello World"
var b = '   Hello world!   '.TrimStart() // b = "Hello world!   "
var c = '   Hello world!   '.TrimEnd() // c = "   Hello world!"

Uppercase/Lowercase
var a = 'The quick brown fox jumps over the lazy dog.'.ToUpper() // a = "THE QUICK BROWN FOX JUMPS OVER THE LAZY DOG."
var b = 'The quick brown fox jumps over the lazy dog.'ToLower() // b = "the quick brown fox jumps over the lazy dog."

Repeat
var a = Enumerable.Repeat("Happy", 3); //a = "Happy Happy Happy"
```

##
Array
---
Js
```
Check all item meets a condition
let a = [1, 30, 39, 29, 10, 13].every((value) => value < 40) // a = true

Filter
let a = [1, 30, 39, 29, 10, 13,45,67].filter((value) => value < 40) // a = [45,67]

Find
let a = [1, 30, 39, 29, 10, 13,45,67].find((element) => element > 10);  // a = 30

FindIndex
let a = [1, 30, 39, 29, 10, 13,45,67].findIndex((element) => element == 10);  // a = 4

ForEach
let a = [1, 30, 39, 29, 10, 13,45,67].forEach((element) => console.log(element));  // a = "1, 30, 39, 29, 10, 13,45,67"

Contains
let a = [1, 30, 39, 29, 10, 13,45,67].includes(1);  // a = true

Count
let a = [1, 30, 39, 29, 10, 13,45,67].length;  // a = 8

Add
let a = [1, 30, 39, 29, 10, 13,45,67].push(9);  // a = [1, 30, 39, 29, 10, 13,45,67,9]

Pop
let a = [1, 30, 39, 29, 10, 13,45,67].pop();  // a = [1, 30, 39, 29, 10, 13,45]

Slice - create shallow copy
let a = [1, 30, 39, 29, 10, 13,45,67].slice(2,4);  // a = [39, 29]
let a = [1, 30, 39, 29, 10, 13,45,67].slice(2);  // a = [39, 29, 10, 13,45,67]

Splice - Remove/update original Array
splice(insertIndex,deletecount,itemToAdd)
Remove
let a = ['Jan', 'March', 'April', 'June'].splice(2,1); // a = ["Jan", "March", "June"]
Update
let a = ['Jan', 'March', 'April', 'June'].splice(3,1,"May"); // a = ["Jan", "March", "April", "May"]
Insert at index
let a = ['Jan', 'March', 'April', 'June'].splice(1,0,"Feb"); // a = ["Jan", "Feb", "March", "April", "June"]

Any
let a = [1, 30, 39, 29, 10, 13,45,67].some((value) => value > 45);  // a = true

Sort
let a = [1, 30, 39, 29, 10, 13,45,67].sort();  // a = [1,10,13,29,30,39,45,67]

Sort Descending
let a = [1, 30, 39, 29, 10, 13,45,67].sort((a,b) => b - a);  // a = [67,45,39,30,29,13,10,1]

Reverse
let a = [1, 30, 39, 29, 10, 13,45,67].reverse();  // a = [67,45,13,10,29,39,30,1]

Transform
let a = [1, 30, 39, 29, 10, 13,45,67].map((value) => value * 2);  // a = [2,60,78,58,20,26,90,134,1]

```

Go
```
import "slices"
import "sort"

Add
a := []int{1,2,3,4,5}
a = append(6,a) // a = [1,2,3,4,5,6]

Length
a := []int{1,2,3,4,5}
c := len(a) // c = 5

Sort Ascending
Integer Sorting
a := []int{5,2,4,3,1}
sort.Ints(s) // a = [1,2,3,4,5]

Float Sorting
s := []float64{5.2, -1.3, 0.7, -3.8, 2.6} // unsorted
sort.Float64s(s) // a = [-3.8 -1.3 0.7 2.6 5.2]

String Sorting
s := []string{"Go", "Bravo", "Gopher", "Alpha", "Grin", "Delta"}
sort.Strings(s) // s = [Alpha Bravo Delta Go Gopher Grin]

Sorting Slices
people := []struct {
		Name string
		Age  int
	}{
		{"Gopher", 7},
		{"Alice", 55},
		{"Vera", 24},
		{"Bob", 75},
	}

sort.Slice(people, func(i, j int) bool { return people[i].Name < people[j].Name }) // By name: [{Alice 55} {Bob 75} {Gopher 7} {Vera 24}]

Custom Datastructure Sorting
type Person struct {
	Name string
	Age  int
}

// ByAge implements sort.Interface based on the Age field.
type ByAge []Person

func (a ByAge) Len() int           { return len(a) }
func (a ByAge) Less(i, j int) bool { return a[i].Age < a[j].Age }
func (a ByAge) Swap(i, j int)      { a[i], a[j] = a[j], a[i] }

func main() {
	family := []Person{
		{"Alice", 23},
		{"Eve", 2},
		{"Bob", 25},
	}
	sort.Sort(ByAge(family))
	fmt.Println(family) // [{Eve 2} {Alice 23} {Bob 25}]
}

// go1.22
slices.Sort(a) // a = [1,2,3,4,5]

Pop
a := []int{1,2,3,4,5,6}
a = a[:len(a)-1]


// For there list function use "github.com/samber/lo". it has a great list of usable functions
```

C#
```
Check all item meets a condition
var a = new List<int>{1,2,3,4,5,6,7,8,9,10}.All(x => x > 7); // a = false

Filter
var a = new List<int>{1,2,3,4,5,6,7,8,9,10}.Where(x => x > 7); // a = [1,2,3,4,5,6]

Find
var a = new List<int>{1,2,3,4,5,6,7,8,9,10}.Find(x => x > 7); // a = 8

FindIndex
var index = new List<int>{1,2,3,4,5,6,7,8,9,10}.FindIndex(x => x > 7);  // index = 7

ForEach
var a = new List<int>{1,2,3,4,5,6,7,8,9,10}.ForEach(x => Console.Write(x));  // a = "1,2,3,4,5,6,7,8,9,10"

Contains
var a = new List<int>{1,2,3,4,5,6,7,8,9,10}.Contains(1);  // a = true

Count
var a = new List<int>{1,2,3,4,5,6,7,8,9,10}.Length;  // a = 10

Add
var a = new List<int>{1,2,3,4,5,6,7,8,9,10}.Add(9);  // a = [1, 30, 39, 29, 10, 13,45,67,9]

Pop
var a = new List<int>{1,2,3,4,5,6,7,8,9,10};  // a = [1, 30, 39, 29, 10, 13,45,67,9]
var b = [1, 30, 39, 29, 10, 13,45,67]Remove(a[a.Length -1]);  // a = [1, 30, 39, 29, 10, 13,45]

Any
var a = new List<int>{1,2,3,4,5,6,7,8,9,10}.Any(x => value > 45);  // a = true
var a = new List<int>{1,2,3,4,5,6,7,8,9,10}.Exist(x => value > 45);  // a = true


Sort Ascending
var a = new List<int>{1,2,3,4,5,6,7,8,9,10}.OrderBy(x => x);  // a = [1,2,3,4,5,6,7,8,9,10]

Sort Descending
var a = new List<int>{1,2,3,4,5,6,7,8,9,10}.OrderByDescending(x => x);  // a = [10, 9, 8, 7, 6, 5,4,3,2,1]

Reverse
var a = new List<int>{1,2,3,4,5,6,7,8,9,10}.Reverse();  // a = [67,45,13,10,29,39,30,1]

Transform
let a = [1, 30, 39, 29, 10, 13,45,67].Select(x => x * 2);  // a = [2,60,78,58,20,26,90,134,1]
```

##
Maps
---

Js
```
Add Key/Value
const map1 = new Map();

map1.set('a', 1); // {'a':1}

Get Value
let b = map1.get('a'); // b = 1

Length
let c = map.size(); // c = 1

Remove
map.delete('a') // delete key/val

Key Exist
map.has('a') // true

Clear
map.Clear()

Foreach
map.forEach((value,key,map) => console.log(`m[${key}] = ${value}`);)

```

Go
```
Add Key/Value
m := map[string]int{"a": 1}
m["b"] = 2

Get Value
let b = m["a"] // b = 1

Length
let c = len(m); // c = 1

Remove
delete(m,'a') // delete key/val

Key Exist
val,ok := m["a"] // val = 1; ok = true

Clear
m = nil

Foreach -- Note maps in golang are unordered
for k, v := range m{
    fmt.Printf("%s:%s", k,v)
}

```


C#
```
Add Key/Value
 var dic = new Dictionary<string, int>
 {
     ["a"] = 1,
 };

dic["b"] = 2 or dic.Add("b", 2);

Get Value
var dic = dic["a"] // b = 1

Length
var c = dic.Count; // c = 1

Remove
var isRemoved = dic.Remove("c") // isRemoved = true if key is present

Key Exist
var exist = dic.ContainsKey("a") // exist = true

Clear
dic.Clear()

Foreach
 foreach (var item in dic)
 {
     Console.WriteLine(item.Key);
 }
```

## 
Loops
---

Js
```
For Index Loop

for (let i = 0; i <= 5; i++) {  // 0, 1, 2, 3, 4, 5
  console.log(i)
}

For of Loop
//You can loop through array/strings
const cars = ["BMW", "Volvo", "Mini"];
for (let x of cars) {
  text += x;
}

For In Loop
//Loop through Object
const person = {fname:"John", lname:"Doe", age:25};
for (let x in person) {
  text += person[x];
}


While Loop
let i = 0

while (i <= 5) {  // 0, 1, 2, 3, 4, 5
  console.log(i)

  i++
}

Do While Loop
let text = ""
let i = 0;

do {
  text += "The number is " + i;
  i++;
}
while (i < 10);
```

Go
```
For Index Loop
--------------
for i := 0; i <= 5; i++ { // 0,1,2,3,4,5
	fmt.Print(i)
}

For Range Loop
--------------
numbers := []int{1,2,3,4,5,6}

//With index and value
for index , num := range numbers{
	fmt.Print(index,num)
}

//With value only
for _ , num := range numbers{
	fmt.Print(num)
}

// With Index only
for index := range numbers{
	fmt.Print(index)
}

// With Maps , key and value
stringnumbers := map[string]int{}
for key , value := range stringnumbers{
	fmt.Print(key,value)
}

//With Value only
for _ , value := range stringnumbers{
	fmt.Print(value)
}

//With Value only
for key := range stringnumbers{
	fmt.Print(key)
}

While Loop
----------
i := 0
for i <= 5 {  // 0,1,2,3,4,5
	fmt.Print(i)
	i++
}
```

C#
```
var numbers = new List<int>{1,2,3,4,5,6}
For Index Loop
for(var i = 0;i < numbers.Length;i++)
{
	Console.WriteLine(i)
}

ForEach
foreach(var e in numbers)
{
	Console.WriteLine(e)
}
```
## 
Switch
---

Js
```
const value = 'b'

switch(value) {
  case 'a':
    console.log('A')
    break
  case 'b':
    console.log('B')
    break
  case 'c':
    console.log('C')
    break
  default:
    console.log('first default')
}
Prints "B"
```

Go
```
value := "b"
switch value {
	case "a":
		fmt.Println("A")
	case "b":
		fmt.Println("B")
	case "c":
		fmt.Println("C")
	default:
		fmt.Println("first default")
}

Prints "B"
```

C#
```
var val = "b";
switch(value) {
  case "a":
    console.log("A")
    break
  case "b":
    console.log("B")
    break
  case "c":
    console.log("C")
    break
  default:
    console.log('first default')
}
Prints "B"
```

## 
String/Int Conversion
---

Js
```
String to Integer

Number function
var x = Number("1000") // x = 1000

parseInt
var x = parseInt("1000", 10); // x = 1000

parseFloat
var x = Math.floor(parseFloat("1000.01")) // x = 1000

Floor
var x = Math.floor("1000.01"); // x = 1000

Round
var x = Math.round("1000") // x = 1000

Unary plus
var x = +"1000"; // x = 1000

Integer to string
let num = 15;
let text = num.toString();
```

Go
```
import "strconv"

String to Integer
 str := "34"
  n , err := strconv.Atoi(str)
  if err != nil{
	fmt.Println(err)
  }
  else{
	fmt.Println(n)
  }

Integer to String
i := 6
strconv.Itoa(i) // 6
```

## 
Template Strings
---

Js
```
let text = `Hello World!`;

Quotes Inside Strings
let text = `He's often called "Johnny"`;

Multiline Strings
let text =
`The quick
brown fox
jumps over
the lazy dog`;

Interpolation
let text = `Welcome ${firstName}, ${lastName}!`;

Expression Substitution
let price = 10;
let VAT = 0.25;

let total = `Total: ${(price * (1 + VAT)).toFixed(2)}`;

Concatenate with +
let text = "cat" + "dog"
```

Go
```
text := `Hello World!`

Quotes Inside Strings
text := `He's often called "Johnny"`

Multiline Strings
str := `This is a
multiline
string.`

Interpolation
name := "bob"
age := 21
message := fmt.Sprintf("%s is %d years old", name, age)
fmt.Println(message)

Concatenate with +
text := "cat" + "dog"
```

C#
```
var text = `Hello World!`;

Quotes Inside Strings
var text = `He's often called "Johnny"`;

Multiline Strings
var str = `This is a
multiline
string.`;

Interpolation
string name = $"My full name is: {firstName} {lastName}";

Concatenate with +
var text = "cat" + "dog";
```
##
Swapping
---

Js
```
let a = 'foo'
let b = 'bar'
console.log(a, b);

[b, a] = [a, b]
console.log(a, b);
```

Go
```
a := "foo"
b := "bar"
fmt.Println(a, b)

b, a = a, b
fmt.Println(a, b)s
```

C#
```
int a = 10;
int b = 2;
(a, b) = (b, a);
```

###
Json
---

Js
```
let jsonstr = '{"foo":"bar"}'
let parsed = JSON.parse(jsonstr)
console.log(parsed)

jsonstr = JSON.stringify(parsed)
console.log(jsonstr)
```

Go
```
import "encoding/json"

type T struct {
	Foo string `json:"foo"`
}

func main() {
	jsonstr := `{"foo":"bar"}`

	t := new(T)
	err := json.Unmarshal([]byte(jsonstr), t)
	if err != nil {
		panic(err)
	}

	fmt.Println(t)

	marshalled, err := json.Marshal(t)
	jsonstr = string(marshalled)
	fmt.Println(jsonstr)
}
```


C#
```
using Newtonsoft

public class MyData
{
}
var jsonString = JsonConvert.SerializeObject(obj);
MyData tmp = JsonConvert.DeserializeObject<MyData>(json);
```

###
Conversion of Primitive Data types to Bytes and vice versa
---

Js
```
Use the following APIs
----------------------
ArrayBuffer
DataView
Uint8Array
Int16Array
TextEncoder
TextDecoder
```

Go
```
Use the following APIs
----------------------
import(
	"bytes"
	"encoding/binary"
)
binary.Read()
binary.Write
bytes.Buffer
encoding/base64
encoding/base32
```

C#
```
Use the following APIs
----------------------
BitConverter
BinaryReader 
BinaryWriter
Encoding.UTF8
MemoryStream
```


###
HttpCalls
---

Js
```
GET
---
fetch('https://jsonplaceholder.typicode.com/posts/1')
  .then(response => response.json()) // Parse JSON from the response
  .then(data => console.log(data))    // Handle the data
  .catch(error => console.error('Error:', error)); // Handle errors

POST
----
fetch('https://jsonplaceholder.typicode.com/posts', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
  },
  body: JSON.stringify({
    title: 'foo',
    body: 'bar',
    userId: 1,
  }),
})
  .then(response => response.json())  // Parse JSON from the response
  .then(data => console.log(data))    // Handle the data
  .catch(error => console.error('Error:', error)); // Handle errors

```

Go
```
GET
---
func main() {
	// Make a GET request
	resp, err := http.Get("https://jsonplaceholder.typicode.com/posts/1")
	if err != nil {
		log.Fatalf("Error making GET request: %v", err)
	}
	defer resp.Body.Close()

	// Read the response body
	body, err := ioutil.ReadAll(resp.Body)
	if err != nil {
		log.Fatalf("Error reading response body: %v", err)
	}

	// Print the response
	fmt.Println(string(body))
}

POST
----
func main() {
	// JSON payload to be sent in the POST request
	data := map[string]interface{}{
		"title":  "foo",
		"body":   "bar",
		"userId": 1,
	}
	jsonData, err := json.Marshal(data)
	if err != nil {
		log.Fatalf("Error marshalling JSON: %v", err)
	}

	// Make a POST request
	resp, err := http.Post("https://jsonplaceholder.typicode.com/posts", "application/json", bytes.NewBuffer(jsonData))
	if err != nil {
		log.Fatalf("Error making POST request: %v", err)
	}
	defer resp.Body.Close()

	// Read and print the response body
	var result map[string]interface{}
	json.NewDecoder(resp.Body).Decode(&result)
	fmt.Println(result)
}
```

C#
```
GET
---
using System;
using System.Net.Http;
using System.Threading.Tasks;

class Program
{
    static async Task Main(string[] args)
    {
        using HttpClient client = new HttpClient();
        
        try
        {
            // Make a GET request
            HttpResponseMessage response = await client.GetAsync("https://jsonplaceholder.typicode.com/posts/1");
            response.EnsureSuccessStatusCode(); // Throw if not a success code.

            // Read the response content as a string
            string responseBody = await response.Content.ReadAsStringAsync();
            
            // Print the response body
            Console.WriteLine(responseBody);
        }
        catch (HttpRequestException e)
        {
            Console.WriteLine($"Request error: {e.Message}");
        }
    }
}


POST
---
using System;
using System.Net.Http;
using System.Text;
using System.Threading.Tasks;
using Newtonsoft.Json; // Install via NuGet (Newtonsoft.Json)

class Program
{
    static async Task Main(string[] args)
    {
        using HttpClient client = new HttpClient();

        // Create the payload
        var postData = new
        {
            title = "foo",
            body = "bar",
            userId = 1
        };

        // Serialize the payload to JSON
        string json = JsonConvert.SerializeObject(postData);

        // Create the request content using StringContent
        StringContent content = new StringContent(json, Encoding.UTF8, "application/json");

        try
        {
            // Make the POST request
            HttpResponseMessage response = await client.PostAsync("https://jsonplaceholder.typicode.com/posts", content);
            response.EnsureSuccessStatusCode();

            // Read and print the response body
            string responseBody = await response.Content.ReadAsStringAsync();
            Console.WriteLine(responseBody);
        }
        catch (HttpRequestException e)
        {
            Console.WriteLine($"Request error: {e.Message}");
        }
    }
}

```



