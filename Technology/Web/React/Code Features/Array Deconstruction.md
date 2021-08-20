Assign a name to a value in a passed in Array

`Const [first, second, third] = 
[
	"one",
	"two",
	"three"
]`

Console.Log(second) would return "two"

Can be done on only single elements of an array e.g


`Const [ , ,third] = 
[
	"one",
	"two",
	"three"
]`

Console.Log(third) would return "three"

The commas are essential for selecting the correct element in the array
