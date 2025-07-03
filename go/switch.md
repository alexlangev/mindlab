## Switch

I always forget how to write them...

Side note, switch in Go breaks by default. Add fallthrough to continue to the next case.

```go
switch i {
case i % 2 == 0:
  fmt.Println("even!")
case i > 100:
  fmt.Println("is big")
  fallthrough
default:
  fmt.Println("odd")
}
```


## Type switches
```go
switch v := i.(type) {
case T:
    // here v has type T
case S:
    // here v has type S
default:
    // no match; here v has the same type as i
}
```


