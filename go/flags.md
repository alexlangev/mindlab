## dealing with flags

```go
// Preprend the usage output (-h or -help)
flag.Usage = func() {
    fmt.Fprintf(flag.CommandLine.Output(), "%s tool. Developed for practice\n", os.Args[0])
    fmt.Fprintf(flag.CommandLine.Output(), "Copyright 2025\n")
    fmt.Fprintln(flag.CommandLine.Output(), "Usage information:")
    flag.PrintDefaults()
}

// define flags (-h is already created by default)
add := flag.Bool("add", false, "Add task to the ToDo list")
complete := flag.Int("complete", 0, "Item to be completed")
filename := flag.Sting("file", "", "Markdown file to preview")

// parse the flags to be able to use the variables
flag.Parse()

// Do stuff with conditionally with flags
fmt.Println(*add)

if *complete > 2 {
    // do something
}

length := len(*filename)

// Slice of non flags arguments
// go run main.go -name Alice -age 25 arg1 arg2 arg3
var x []string = flag.Args() // ["arg1", "arg2", "arg3"]

// Print default usage message for a program that uses the flag package
flag.Usage()
```
