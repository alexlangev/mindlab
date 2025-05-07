# Slices
```go
// slice literals
var x = []int{10, 20, 40}

// sparse slice
var y = []int{10, 4:1, 9:55} // [10 0 0 0 1 0 0 0 0 55]

// multidimensional slice
var y = [][]int

// zero-value (nil) slice
var x []int
```

## comparing slices
Slices are not directly comparable. To do so, the *Eqal* function of the *slices* packages is needed.

```go
var b = []string{"alex", "sara"}

fmt.Println(slices.Equal(a, b)) // true
```
