# Libft - C Library

 Libft is a C library project that includes replicas of some standart library functions in C and some additional ones that I coded.  
 I use this library in most of my C projects.

 ## Usage
 `make` to compile the library (libft.a)<br>
 `make bonus` to compile the library with bonus functions


 ## Functions

Each function in the library is prefixed with 'ft_' and named to mirror the function it replicates.<br>

| header   | 0 |
| -------- | -------- |
|strings.h|[ft_bzero](./ft_bzero.c)|

| header   | 0 | 1 |
| -------- | -------- | --------- |
|stdlib.h|[ft_atoi](./ft_atoi.c)|[ft_calloc](./ft_calloc.c)|


| header   | 0 | 1 | 2 | 3 |
| -------- | -------- | --------- | -------- | -------- |
|ctype.h|[ft_isalpha](./ft_isalpha.c)|[ft_isalnum](./ft_isalnum.c)|[ft_isascii](./ft_isascii.c)|[ft_isprint](./ft_isprint.c)|[ft_toupper](./ft_toupper.c)|[ft_tolower](./ft_tolower.c)|

| header   | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 |
| -------- | -------- | --------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- |
|string.h|[ft_strlen](./ft_strlen.c)|[ft_memset](./ft_memset.c)|[ft_memcpy](./ft_memcpy.c)|[ft_memmove](./ft_memmove.c)|[ft_strlcpy](./ft_strlcpy.c)|[ft_strlcat](./ft_strlcat.c)|[ft_strchr](ft_strchr.c)|[ft_strncmp](./ft_strncmp.c)|[ft_memchr](./ft_memchr.c)|[ft_memcmp](./ft_memcmp.c)|[ft_strnstr](./ft_strnstr.c)|[ft_strdup](./ft_strdup.c)


## Additional Functions
Since these functions either aren't standart library functions or work different than their originals, I've included explanations for each.<br>
| name   | prototype | parameters | return value | description |
| -------- | -------- | --------- | -------- | -------- |
| [ft_substr](./ft_substr.c) | char  *ft_substr(char const *s, unsigned int start, size_t len) | s: The original string from which to create the substring.<br><br>start: The starting index of the substring within ’s’.<br><br>len: The maximum length of the substring | The substring.<br>NULL if the allocation fails. | Allocates memory (using malloc(3)) and returns a substring from the string ’s’.<br>The substring starts at index ’start’ and has a maximum length of ’len’
| [ft_strjoin](./ft_strjoin.c) | char *ft_strjoin(char const *s1, char const *s2) | s1: The prefix string<br><br>s2: The suffix string | The new string.<br>NULL if the allocation fails. | Allocates memory (using malloc(3)) and returns a new string, which is the result of concatenating ’s1’ and ’s2’.
| [ft_strtrim](./ft_strtrim.c) | char *ft_strtrim(char const *s1, char const *set) | s1: the string to be trimmed<br><br>set: The string containing the set of characters to be removed | The trimmed string.<br>NULL if the allocation fails. | Allocates memory (using malloc(3)) and returns a copy of ’s1’ with characters from ’set’ removed from the beginning and the end.
| [ft_split](./ft_split.c) | char **ft_split(char const *s, char c) | s: The string to be split<br><br>c: The delimiter character | The array of new strings resulting from the split.<br>NULL if allocation fails. | Allocates memory (using malloc(3)) and returns an array of strings obtained by splitting ’s’ using the character ’c’ as a delimiter. The array must end with a NULL pointer.
| [ft_itoa](./ft_itoa.c) | char *ft_itoa(int n) | n: The integer to convert. | The string representing the integer.<br>NULL if the allocation fails. | Allocates memory (using malloc(3)) and returns a string representing the integer received as an argument. Negative numbers must be handled.
| [ft_strmapi](./ft_strmapi.c) | char *ft_strmapi(char const *s, char (*f)(unsigned int, char)) | s: The string to iterate over<br><br>f: The function to apply to each character | The string created from the successive applications of ’f’.<br>NULL if allocation fails. | Applies the function f to each character of the string s, passing its index as the first argument and the character itself as the second. A new string is created (using malloc(3)) to store the results from the successive applications of f.
| [ft_striteri](./ft_striteri.c) | void ft_striteri(char *s, void (*f)(unsigned int, char\*)) | s: The string to iterate over.<br><br>f: The function to apply to each character. | - | Applies the function 'f' to every character in 's'. The difference from [ft_strmapi](./ft_strmapi.c) is that this function modifies the original string directly instead of making a modified copy.<br>Applies the function ’f’ to each character of the string passed as argument, passing its index as the first argument. Each character is passed by address to ’f’ so it can be modified if necessary.
| [ft_putchar_fd](./ft_putchar_fd.c) | void ft_putchar_fd(char c, int fd) | c: The character to output.<br><br>fd: file descriptor for output | - | Outputs the character 'c' to file descriptor 'fd'.
| [ft_putstr_fd](./ft_putstr_fd.c) | void ft_putstr_fd(char *s, int fd) | s: The string to output.<br><br>fd: The file descriptor on which to write. | - | Outputs the string ’s’ to the specified file descriptor.
| [ft_putendl_fd](./ft_putendl_fd.c) | void ft_putendl_fd(char *s, int fd) | s: The string to output.<br><br>fd: The file descriptor on which to write. | - | Outputs the string 's' and a newline character ('\n') to file descriptor 'fd'.
| [ft_putnbr_fd](./ft_putnbr_fd.c) | void ft_putnbr_fd(int n, int fd) | n: integer to be printed<br><br>fd: file descriptor for output | - | Outputs the string ’s’ to the specified file descriptor followed by a newline.

## Bonus Functions

The bonus functions in this library are functions for creating and manipulating linked lists.<br>
You can find the definition of t_list in [the header file](./libft.h).

| name   | prototype | parameters | return value | description |
| -------- | -------- | --------- | -------- | -------- |
| [ft_lstnew](./ft_lstnew_bonus.c) | t_list *ft_lstnew(void *content) | content: The content to store in the new node. |A pointer to the new node | Allocates memory (using malloc(3)) and returns a new node. The ’content’ member variable is initialized with the given parameter ’content’. The variable ’next’ is initialized to NULL.
| [ft_lstadd_front](./ft_lstadd_front_bonus.c) | void ft_lstadd_front(t_list **lst, t_list *new) | lst: The address of a pointer to the first node of a list.<br><br>new: The address of a pointer to the node to be added. | - | Adds the node ’new’ at the beginning of the list.
| [ft_lstsize](./ft_lstsize_bonus.c) | void ft_lstadd_back(t_list **lst, t_list *new) | lst: The beginning of the list. | The length of the list | Counts the number of nodes in the list.
| [ft_lstlast](./ft_lstlast_bonus.c) | t_list *ft_lstlast(t_list *lst) | lst: The beginning of the list. | Last node of the list | Returns the last node of the list.
| [ft_lstadd_back](./ft_lstadd_back_bonus.c) | char *ft_itoa(int n) | lst: The address of a pointer to the first node of a list.<br><br>new: The address of a pointer to the node to be added. | - | Adds the node ’new’ at the end of the list.
| [ft_lstdelone](./ft_lstdelone_bonus.c) | void ft_lstdelone(t_list *lst, void (*del)(void\*)) | lst: The node to free.<br><br>del: The address of the function used to delete the content.|-| Takes a node as parameter and frees its content using the function ’del’. Free the node itself but does NOT free the next node.
| [ft_lstclear](./ft_lstclear_bonus.c) | void ft_lstclear(t_list **lst, void (*del)(void\*)) | lst: The address of a pointer to a node.<br><br>del: The address of the function used to delete the content of the node.| - | Deletes and frees the given node and all its successors, using the function ’del’ and free(3). Finally, set the pointer to the list to NULL.
| [ft_lstiter](./ft_lstiter_bonus.c) | void ft_lstiter(t_list *lst, void (*f)(void *)) | lst: The address of a pointer to a node.<br><br>f: The address of the function to apply to each node’s content. | - | Iterates through the list ’lst’ and applies the function ’f’ to the content of each node.
| [ft_lstmap](./ft_lstmap_bonus.c) | t_list	*ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *)) | lst: The address of a  ointer to a node.<br><br>f: The address of the function applied to each node’s content.<br><br>del: The address of the function used to delete a node’s content if needed.| The new list.<br>NULL if the allocation fails. | Iterates through the list ’lst’, applies the function ’f’ to each node’s content, and creates a new list resulting of the successive applications of the function ’f’. The ’del’ function is used to delete the content of a node if needed.
