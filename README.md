# get_next_line

## Description
get_next_line is a project developed as part of the curriculum at 42 school. The goal of this project is to create a function that reads a line from a file descriptor, either from a file, from the standard input (stdin), or from any other valid file descriptor.

## Features
- Reads a line from a file descriptor
- Dynamically allocates memory to store read lines
- Works with files, standard input (stdin), or any other valid file descriptor

## Usage
To use get_next_line in your project, include the "get_next_line.h" header file and call the get_next_line function.

Example:
```c
#include "get_next_line.h"

int main()
{
    int fd;
    char *line;

    fd = open("example.txt", O_RDONLY);
    while (get_next_line(fd, &line) > 0)
    {
        printf("%s\n", line);
        free(line);
    }
    close(fd);
    return 0;
}
```

## Installation
To compile the get_next_line function along with your project, you need to include the "get_next_line.c" file and compile it along with your other source files.
