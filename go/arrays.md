# Arrays

## Declaration

```go
// zero-value array
var x [3]int

// array literal
var y = [3]int{10, 20, 30}
var y = [...]rune{'a', 'b', 'c', 'd'}

// sparse array 
var z  = [10]int{1, 5:4, 9:55} // [1 0 0 0 0 4 0 0 0 55]
```

## lengths

[3]int and [4]int are two different types in go!!!

