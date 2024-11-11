<h1 align=center>💻 Get Next Line</h1>
<p align="center">
  <img src="img/get_next_line.png?raw=true" alt="Get Next Line Project Image"/>
</p>

## About
>This project is about programming a function that returns a line read from a file descriptor.

[Subject Get_next_line Project 42](Get_next_line.pdf)

The function `get_next_line` reads a line from a valid file descriptor, continuing until it reaches the end of the line (`\n` character) or the end of the file.

## Features
- **Description**: Reads from a valid file descriptor until the end of the line, returning one line at a time.
- **Feature**: Enhances file reading by managing memory efficiently, performing multiple reads as needed to reach the end of the line, and preserving any remaining content for the next call.
- **How to Use**: Call the function `get_next_line` with a valid file descriptor as first argument.Continue calling it until the function returns `NULL`, which indicates the end of the file.

## Setup

**Clone the Repository**:

```bash
git clone https://github.com/J0hann3/get_next_line.git
cd get_next_line
```

## Usage

- Use the `get_next_line()` function by passing a valid file descriptor as the first argument.
- Include the following line in your file to access the function:
```bash
#include "get_next_line.h"
```
- Modify the buffer length used to read the file by compiling with `-D BUFFER_SIZE=<size>`.
- `get_next_line` returns a `char *` containing the next line read from the file. It returns NULL when the end of the file is reached.

Here is an example of how to use `get_next_line` in a loop to read through an entire file:

```c
#include "get_next_line.h"

int main() {
  int fd = open("example.txt", O_RDONLY);
  if (fd < 0)
    return 1;

  char *line;
  while ((line = get_next_line(fd)) != NULL) {
      printf("%s\n", line);
      free(line);
  }

  close(fd);
  return 0;
}
```

## New Notion

### Static Variables
- Static variables retain their value even after the end of their scope, meaning they maintain their value across multiple function calls.
- Static variables are stored in the data segment, not the stack.
```C
static data_type var_name = var_value;
```
- The variable is first initialized with `var_value`.

### Compiler define
- Specify the value of a define during compilation
```bash
-D DEFINE_NAME=<defined_value>
```
- In the code, define the default value to ensure the program runs correctly without errors:
```C
# ifndef DEFINE_NAME
#  define DEFINE_NAME define_value
# endif
```

### lseek
- The `lseek` changes the file offset but was not allowed in this project.