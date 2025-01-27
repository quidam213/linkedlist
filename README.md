# linkedlist
Basic library linked list in C.

I used this in my recode of ls project and also the library version of it in my sokoban project.


### How to use it in your project ?

Clone the repository or download it.

Use the Makefile to build the library linkedlist.a
```bash
> make          # build the lib
> make re       # rebuild if it exists
> make clean    # clean the tmp file
> make fclean   # clean all, also the lib
```

Include the linkedlist.h in your c file.
```c
#include "linkedlist.h"
```

Use the library as you wish
```c
list_t *head = NULL;
char *a = "Hello";
char *b = "World!";
add_element(&head, (void *)a, &base_free_node);
add_element(&head, (void *)b, &base_free_node);

for (list_t *tmp = head; tmp; tmp = tmp->next) {
    printf("%s%c", (char *)tmp->data, tmp->next ? ' ' : '\n');
}
```

Then compile your code with the library.
```
gcc main.c -L. -l:linkedlist.a
```

Execute your binary !

```bash
> ./a.out
> Hello World!
>
```

You can see some example in my ls or sokoban project as i said earlier.
But I suggere you to see my ls more than my sokoban for that library.

### Author
dam, github : quidam213
