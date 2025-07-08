# Strings
Go uses fstrings like in C. It's shit...

%v prints the Go syntax representation of a value, it's a nice default.
%s prints a string
%d prints an int
%.2f prints a float with 2 decimals
%t prints a bool

### return formated string
```go
const name = "Saul Goodman"
const openRate = 30.5
msg := fmt.Sprintf("Hi %s, your open rate is %.1f percent\n", name, openRate)
```

### print formated string
```go
username := "Alex"
fmt.Printf("Hello %s", username)
```


## Convert to string

Integers to strings

```go
import "strconv"

n := 5
s := strconv.Itoa(n)
```
