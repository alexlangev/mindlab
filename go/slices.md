# Slices

Unlike arrays, the length is not part of the type. They can grow.

```go
var y = []int{1, 2, 0, 0, 4} // slice literal
fmt.Println(y)

var z = [5]int{1, 2, 4: 4} // sparse slice. All 0 except the indexes specified
fmt.Println(z)

var x = [][]int{} // 2d array

var empty []int == nil // true
```


## Built-ins
```go
x := []int{1, 2, 3}
len(x) // 3
cap(x) // 3
// appending will increase the capacity by double its current value?
```


## Comparing slices

Can't compare slices using `==` like with arrays. The slices package has what you need.

```go
x := []int{1, 2, 3}
y := []int{1, 2, 3}

slices.Equal(x, y) // true
```


## Append

```go
var x = []int{1, 2, 3}
x = append(x, 4)
x = append(x, 5, 6, 7)

var y = []int{8, 9, 10}
x = append(x, y...)
```


## Make

You can create slices with specific capacities to optimize your code.

```go
x := make([]int, 5) // [0, 0, 0, 0, 0]
```


## Clearing slices

You can clear slices. They keep their length and capacity but all values are their zero-vales.

```go
var x = []int{1, 2, 3}
clear(x) == [0, 0, 0]
```


## Subslices

Sublices share a similar notation with Python. 

!!! The sublice shares memory with original slice. Changing one will update the other!

```go
x := []int{1, 2, 3, 4, 5}
fmt.Println(x[1:3]) // prints [2, 3]
```
