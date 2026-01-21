*This project has been created as part of the 42 curriculum by mperrine.*

`get_next_line` is a project from the 42 curriculum that implements a function to read a single line from a file descriptor. The function returns one line at a time, no matter the length, and can handle multiple file descriptors simultaneously (bonus part).

The function reads from:
- Files
- Standard input
- Any valid file descriptor

Each call to `get_next_line` returns the next line, including the newline character `\n` (except for the last line if it doesn't end with one).

## Instructions

Include the header in your C file:
```c
#include "get_next_line.h"
```
or
```c
#include "get_next_line_bonus.h"
```

Basic usage:
```c
char *line;
int  fd;

fd = open("file.txt", O_RDONLY);
line = line = get_next_line(fd);
while (line)
{
    printf("%s", line);
    free(line);
    line = line = get_next_line(fd);
}
close(fd);
```

## Resources

This project was developed without the use of any AI tools.
