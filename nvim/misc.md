## find documentation of a word
enter K when cursor on a word

## Jump to subject and come back... 
when do you use this other than in documentation?

jump to subject: ctrl-]
jump back ctrl-o

## DELETION

x -> delete character
dw -> delete from cursor to start of next word
de -> delete from cursor to the end of the current word
d$ -> delete from cursor to end of line
d^ -> delete from cursor to begining of line keeps indentation
d0 -> delete from cursor to begining of line
dd -> delete entire line

d and x are **operators**
w, e, $, ^, 0, d are **motions**

### using counts

operator + count + motion
d 2 w (delete from cursor to the start of the 2nd to next word)

2dd will delete current and following line


## undo redo
u undo latest change
U reset line to original state
ctrl-r redo latest change


NEXT UP lesson 3 vim tutor
