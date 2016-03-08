# Toweldocs
This repository contains various bits of documentation for Towel: a tutorial, code examples, a command list, and a more formal description of the language.


## Command list
### Stack operations
Command   | Description                                             | Implemented?
----------|---------------------------------------------------------|--------------
*number*  | Pushes *int* to the stack.                              | yes
*"string"*| Pushes the ascii codes of *string* to the stack.        | yes
drop      | Pops the top value and discards it.                     | yes
dup       | Pops the top value and pushes it to the stack two times.| yes
rand      | Pushes a random value (0-99) to the stack.              | yes
rev       | Reverses the entire stack.                              | yes
raise     | Puts the top value on the bottom of the stack           | yes
lower     | Puts the bottom value on the top of the stack           | yes

### Math
Command | Alias | Description                                                               | Implemented?
--------|-------|---------------------------------------------------------------------------|--------------
add     | +     | Pops the two top values and pushes their combined value.                  | yes
sub     | -     | Pops the two top value and pushes the second highest minus the top value. | yes
mul     | *     | Pops the two top values and pushes their multiplied value.                |
div     | /     | Pops the two top value and pushes the second highest devised by top value.| Fabric (alias only)
mod     | %     | Modulo                                                                    |

###I/O
Command | Alias | Description                                                                 | Implemented?
--------|-------|-----------------------------------------------------------------------------|--------------
put     | ,     | Prints the top value to the stdout.                                         | yes (no alias)
chr     | .     | Prints the ascii character with top value code to the stdout.               | yes (moisture: no alias, as putchr
nput    |       | Prints the top value to the stdout with a newline.                          | moisture
nputchr |       | Prints the ascii character with top value code to the stdout with a newline.| moisture
grab    |       | Asks the user for input (which can be a character, string, or number).      | yes

###Loops
Command | Alias | Description                                                                 | Implemented?
--------|-------|-----------------------------------------------------------------------------|--------------
sloop   | [     | Marks the beginning of a loop.                                              | yes (alias only)
eloop   | ]    | Marks the ending of a loop. The instruction pointer jumps back to the matching sloop, unless the stack is empty or the top value is 0.                                                                        | yes (alias only)
neloop  | !]   | Marks the ending of a loop. The instruction pointer jumps back to the matching sloop if stack is empty or the top value is 0. |
break   |      | Exits current loop without completing it.                                    | Fabric
continue|      | Goes to beginning of loop.                                                   |

### Gotos
Deprecated
Command | Description                                                                 | Implemented?
--------|-----------------------------------------------------------------------------|--------------
lbl *x* | Creates a label at the current line with name *x*. Can only be used on a line of its own. | moisture
goto *x*| Moves the instruction pointer to label *x*. | moisture

### Other
Command | Description                                                                 | Implemented?
--------|-----------------------------------------------------------------------------|--------------
dump    | Prints the entire stack to the stdout.                                      | yes
end     | Stops the program, appends a newline to the stdout, and exits with code 0.  | yes


![Towel](https://raw.githubusercontent.com/Towellang/Toweldocs/master/logo.png)
