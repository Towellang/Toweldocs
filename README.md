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
nput    |       | Prints the top value to the stdout with a newline.                          | moisture
nputchr |       | Prints the ascii character with top value code to the stdout with a newline.| moisture
grab    |       | Asks the user for input (which can be a character, string, or number).      | moisture (with excess arg)

###Loops
Command | Alias | Description                                                                 | Implemented?
--------|-------|-----------------------------------------------------------------------------|--------------
sloop   | [     | Marks the beginning of a loop.                                              | moisture (alias only)
eloop   | ]    | Marks the ending of a loop. The instruction pointer jumps back to the matching sloop, unless the stack is empty or the top value is 0.                                                                        | moisture (alias only)
neloop  | !]   | Marks the ending of a loop. The instruction pointer jumps back to the matching sloop if stack is empty or the top value is 0. |

### Gotos
Command | Description                                                                 | Implemented?
--------|-----------------------------------------------------------------------------|--------------
lbl *x* | Creates a label at the current line with name *x*. Can only be used on a line of its own. | moisture
goto *x*| Moves the instruction pointer to label *x*. | moisture

### Other
Command | Description                                                                 | Implemented?
--------|-----------------------------------------------------------------------------|--------------
dump    | Prints the entire stack to the stdout.                                      | moisture (as 'debug')
end     | Stops the program, appends a newline to the stdout, and exits with code 0.  | moisture


![Towel](https://raw.githubusercontent.com/Towellang/Toweldocs/master/logo.png)
