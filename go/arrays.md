# Arrays

Arrays are too rigid for common use. The length of the array is part of it's type. Therefore `[2]int` and `[3]int` aren't the same type and there is not type conversion between the two.

Arrays are good when you know the size in advance. Using them will optimize memory allocation and stuff.

```go
var x [3]int // zero array
fmt.Println(x)

var y = [5]int{1, 2, 0, 0, 4} // array literal
fmt.Println(y)

var y2 = [...]int{1, 3, 5, 6, 7, 8, 0} // don't need to specify the length when using an array literal
fmt.Println(y2)

var z = [5]int{1, 2, 4: 4} // sparse array. All 0 except the indexes specified
fmt.Println(z)

fmt.Println(y == z) // true
```
