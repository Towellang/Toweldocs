# Toweldocs
This repository contains various bits of documentation for Towel: a tutorial, code examples, a command list, and a more formal description of the language.

## Command list
### Stack operations
Command  | Description                                             | Implemented?
---------|---------------------------------------------------------|--------------
*number* | Pushes *int* to the stack.                              | moisture
"*word*  | Pushes the ascii codes of *word* to the stack.          | moisture
drop     | Pops the top value and discards it.                     | moisture (as 'pop')
dup      | Pops the top value and pushes it to the stack two times.| moisture
rand     | Pushes a random value (0-99) to the stack.              | moisture
rev      | Reverses the entire stack.                              | moisture
raise    | Puts the top value on the bottom of the stack           | moisture
lower    | Puts the bottom value on the top of the stack           | moisture

### Math
Command | Alias | Description                                                               | Implemented?
--------|-------|---------------------------------------------------------------------------|--------------
add     | +     | Pops the two top values and pushes their combined value.                  | moisture
sub     | -     | Pops the two top value and pushes the second highest minus the top value. | moisture
mul     | *     | Pops the two top values and pushes their multiplied value.                |
div     | /     | Pops the two top value and pushes the second highest devised by top value.|
mod     | %     | Modulo                                                                    |

###I/O
Command | Alias | Description                                                                 | Implemented?
--------|-------|-----------------------------------------------------------------------------|--------------
put     | ,     | Prints the top value to the stdout.                                         | moisture (no alias)
putchr  | .     | Prints the ascii character with top value code to the stdout.               | moisture (no alias)
nput    |       | Prints the top value to the stdout with a newline.                          | moisture (no alias)
nputchr |       | Prints the ascii character with top value code to the stdout with a newline.| moisture (no alias)
