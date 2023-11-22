# Get_next_line

>This project is about programming a function that returns a line read from a file descriptor.

[Subject Get_next_line Project 42](https://cdn.intra.42.fr/pdf/pdf/105477/en.subject.pdf)

## Compilation
```
git clone
gcc -Wall -Wextra -Werror get_next_line.c get_next_line_utils.c main.c -o get_next_line
```
You need to create a main to test or use this programm.  

To use this function in your code, you can include this
```
#include "get_next_line.h
```

With `-D BUFFER_SIZE=<size>` you can modifie the lenght of the buffer use to read the file.
