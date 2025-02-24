# Libft - C Library

 Libft is a C library projects that includes replicas of some standart library functions in C and some additional ones that I myself coded.  
 I use this library in most of my C projects.

 ## Usage
 `make` to compile the library (libft.a)  
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

| name   | prototype | parameter | parameter | return | desc |
| -------- | -------- | --------- | -------- | -------- | -------- |
| [ft_substr](./ft_substr.c) | char  *ft_substr(char const *s, unsigned int start, size_t len) |
