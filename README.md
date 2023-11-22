# Get_next_line

>This project is about programming a function that returns a line read from a file descriptor.

[Subject Get_next_line Project 42](https://cdn.intra.42.fr/pdf/pdf/105477/en.subject.pdf)

## Compilation

You need to create a main to test or use this programm.  
```
git clone https://github.com/J0hann3/get_next_line.git
gcc -Wall -Wextra -Werror get_next_line.c get_next_line_utils.c main.c -o get_next_line
```

To use this function in your code, you can include this
```
#include "get_next_line.h
```

With `-D BUFFER_SIZE=<size>` you can modify the lenght of the buffer use to read the file.
