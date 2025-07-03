# numerical types

uint8 and byte are the same.

int is a int64 on 64 bit cpus while an int32 on 32bit cpus. 
Isn't that risky?

## floats

In go we got float32 and float64

Never compare floats in your app. Floats aren't precise. Use a max allowed difference instead.


## complex

complex128 uses two float64
complex64 uses two float32

```go
x := complex128(2.8, -1003.5)

fmt.Println(real(x))
fmt.Println(real(y))
```
