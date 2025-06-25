# Delete

x deletes characters
dd deletes lines
J deletes linebreak


# Undo Redo

u undo last change
ctrl + r redo last change
U undo last edited line


# Opening a newline

o creates a new empty line below the cursor and switch to insert mode.
O creates a new empty line above the cursor and switch to insert mode.


# go to tag

ctrl+] jump to tag
ctrl+o jump back (repeat to go further back)
ctrl+T pop tag (jump back)   ???

# Word movement

w   forward one word (to first char)
e   forward one word (to last char)

b   backwards one word (to first char)
ge   forward one word (to last char)


# Character movement

f_  forward to next _
t_  forward to char previous of the next _

F_  backwards to previous _
T_  backwards to char previous of the next _


# Move to line

_G  Move to line _
G   Move to last line
gg  Move to first line


## Search

/the    search for "*the*"
/the\>  search for "*the" (word ends with the)
/\<the  seatch for "the*" (word starts with the)


I'm at 3.10...
