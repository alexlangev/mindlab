# Unix basics

Master the following

## basic commands

- cat
- ls
- cp
- mv
- touch
- rm
- echo
- pwd

## navigation

- cd
- mkdir
- rmdir

## globs (wildcards)

* matches any string

`echo *` prints out all files and directories in the current dir.

`echo a*` prints out all files and directories in the current dir that starts with a

`echo *a*` prints out all files and directories in the current dir that contains a

? matches a single character (* matches any number of characters)

## grep the super useful command

```shell
# prints the lines from passwd that contains the string "root"
grep root /etc/passwd
```

learn the following flags:

- i
- v
- E

## other commands

- less
- head
- tail
- pwd
- diff
- file
- find
    `find dir -name filename -print`
- sort

## changing password

`passwd`

## Environment variables

## Shell variables

Holds strings as a variable. Not saved between terminal instances.
