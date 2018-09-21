# GET NEXT LINE
  
Get Next Line is a function that reads a file line by line
It is an individual project at 42 school

## Built With

C language

## Return Value
 
* Return 1 when it read a line
* Return 0 when it finished reading a file
* Return -1 when an error occurs
 
## Running
 
* Create a main.c

```
#include "get_next_line.h"

int		main(int ac, char **av)
{
	char *line;
	int fd;

	line = NULL;;
	if (ac == 2)
	{
		fd = open(av[1], O_RDONLY);
		while (get_next_line(fd, &line) != 0)
		{
			printf("%s\n", line);
			free(line);
		}
	}
	return (0);
}
```

* Git clone https://github.com/jsauron/get-next-line.git 
* cd GNL

```
gcc main.c get_next_line.c libft/libft.a
/a.out example.txt
```

## Author

**Jeanne Sauron**
