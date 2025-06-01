## importing

External go modules are essentially what npm packages are.

You import them into your go project like this. This command will add the module as a dependency in the go.mod file

```go
go get github.com/russross/blackfriday/v2
```

This will make it accessible to your to project and locks the version you need???
