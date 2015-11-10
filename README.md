# Toweldocs
This repository contains various bits of documentation for Towel: a tutorial, code examples, a command list, and a more formal description of the language.

## Command list
Command     | Alias | Description                                             | Implemented?
------------|-------|---------------------------------------------------------|--------------
**number**  |       | Pushes **int** to the stack.                            | moisture
"**word**   |       | Pushes the ascii codes of **word** to the stack.        | moisture
drop        |       | Pops the top value and discards it.                     | moisture (as 'pop')
dup         |       | Pops the top value and pushes it to the stack two times.| moisture
rand        |       | Pushes a random value (0-99) to the stack.              | moisture
rev         |       | Reverses the entire stack.                              | moisture
raise       |       | Puts the top value on the bottom of the stack           | moisture
lower       |       | Puts the bottom value on the top of the stack           | moisture
add         | +     | Pops the two top values and pushes their combined value.| moisture
sub         | -     | Pops the two top value and pushes the second highest minus the top value | moisture
