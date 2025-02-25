# Libft - C Library

 Libft is a C library projects that includes replicas of some standart library functions in C and some additional ones that I coded.  
 I use this library in most of my C projects.

 ## Usage
 `make` to compile the library (libft.a)<br>
 `make bonus` to compile the library with bonus functions


 ## Functions

Each function in the library is prefixed with 'ft_' and named to mirror the function it replicates.

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

| name   | prototype | parameters | return | desc |
| -------- | -------- | --------- | -------- | -------- |
| [ft_substr](./ft_substr.c) | char  *ft_substr(char const *s, unsigned int start, size_t len) | s: the parent string<br><br>start: the starting index of the substring inside the parent string<br><br>len: the maximum length of the substring | Substring.<br>NULL if allocation fails. | Allocates memory with malloc(3) and returns a substring derived from "s". The substring starts from the "start" index of "s" and the max length of it is "len".
| [ft_strjoin](./ft_strjoin.c) | char *ft_strjoin(char const *s1, char const *s2) | s1: prefix string<br><br>s2: suffix string | concatenated string.<br>NULL if allocation fails. | Allocates memory with malloc(3) and and returns the string made by concatenating 's1' and 's2'.
| [ft_strtrim](./ft_strtrim.c) | char *ft_strtrim(char const *s1, char const *set) | s1: the string that would be trimmed<br><br>set: character to trim from s1
| [ft_split](./ft_split.c) | char **ft_split(char const *s, char c) | s: the string to be split<br><br>c: separator character
| [ft_itoa](./ft_itoa.c) | char *ft_itoa(int n) | n: integer value to be converted
| [ft_strmapi](./ft_strmapi.c) | char *ft_strmapi(char const *s, char (*f)(unsigned int, char)) | s: string to iterate through<br><br>f: the function to be applied to every character of s
| [ft_striteri](./ft_striteri.c) | void ft_striteri(char *s, void (*f)(unsigned int, char\*)) | s: string to iterate through<br><br>f: the function to be applied to every character of s
| [ft_putchar_fd](./ft_putchar_fd.c) | void ft_putchar_fd(char c, int fd) | c: character to be printed<br><br>fd: file descriptor for output
| [ft_putstr_fd](./ft_putstr_fd.c) | void ft_putstr_fd(char *s, int fd) | s: string to be printed<br><br>fd: file descriptor for output
| [ft_putendl_fd](./ft_putendl_fd.c) | void ft_putendl_fd(char *s, int fd) | s: string to be printed<br><br>fd: file descriptor for output
| [ft_putnbr_fd](./ft_putnbr_fd.c) | void ft_putnbr_fd(int n, int fd) | n: integer to be printed<br><br>fd: file descriptor for output
