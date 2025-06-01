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

Holds strings as variables. Not specific to a single shell. Child process will have access.

## Shell variables

Holds strings as a variable. Not saved between terminal instances.

## Command path

```go
# append or prepend dir to the path environment variable
PATH=dir:$PATH
PATH=$PATH:dir
```

## shell input and output

redirecting the output of a command to a file

```sh
# overides the current content of the file
command > file

# append at the end of the file instead of clobbering it
command > file

# redirect standard error with "2>"
command 2> file
```

redirecting the output to the input of another command

```sh
command1 | command2
```

## Managing processes
List processes with

```sh
# Try 'ps --help <simple|list|output|threads|misc|all>'
ps -s
```

Kill stop and continue
```sh
# kill process same as CTRL-C
kill pid

# freeze and continues
kill -STOP pid
kill -CONT pid
```

## job control
`jobs` is a command. It lists the active jobs.

adding `&` after the command will "detach" it from the terminal. This gives you your terminal back when running some long standing process. 

```sh
# finally no more detaching tmux sessions!
keymapp &
```
