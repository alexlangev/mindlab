# TODOs

## Pass by values
Be able to explain what pass by value is.

Go is pass by value except for which types?

What are the traps that comes with this?

Any useful stuff for leetcode here?

Compare with JS.

When do pointers come into play?


## Named returns, explicit returns and naked returns

More a stylistic change than anything else. Can be cool.

Naked returns are harder to read?


## First class functions, higher order functions, funcitons as values
What are they?
We like them or not?
Why reach for them?
Traps? 
Tricks?


## Anonymous functions
When do we use them?

Get used to reading and writing them.


## Closures
Talking about them
When to use them


## defer

High level explanation


## () after a function to call it directly


## Scopes in go

block, package, global

Be able to talk about it and explain

## Closures

Why are they used in CS?

## Currying

Why, how?
Like Haskel right?


## anonymous structs

When should I reach for them?


## Embedded vs nested structs

### nested stucts
```go
type human {
  profession string
  age int
}

type castle {
  numOfTowers int
  guard human
}
```

### Embedded stucts

```go
type human {
  profession string
  age int
}

type blacksmith {
  numOfhammers int
  human
}
```


## Memory layout of structs

In general don't worry too much. Order from big to small might optimize the memory usage.

## Empty structs in go

Empty structs are used in go as unary values. They hold 0 bytes instead of a 1 byte bool.

## Interfaces

When is it a good idea to use them?

They are implemented implicitly.

A type can implement more than one interface. That's fine.

Explain how interfaces are not classes in go. What is the difference?

Blog: https://blog.boot.dev/golang/golang-interfaces/?_gl=1*6tc9cr*_gcl_au*MTk4NDIwNzY0NC4xNzUxMDc5Njk0*_ga*MTE3Mjc1NjM5Ny4xNzUxMDc5Njk0*_ga_M7P2PBGN8N*czE3NTE1MDE0ODkkbzkkZzEkdDE3NTE1MDUxMTAkajYwJGwwJGgxNDMxMTQxMjk2

Know the following interfaces:
- Error
- Stringer

## Polymorphism

Polymorphism comes into play in go with interfaces. Learn the theory and be able to explain it.
