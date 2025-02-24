# Libft - C Library

 Libft is a C library projects that includes replicas of some standart library functions in C and some additional ones that I myself coded.  
 I use this library in most of my C projects.

 ## Usage
 `make` to compile the library (libft.a)  
 `make bonus` to compile the library with bonus functions

 ## Functions

Each function in the library is prefixed with 'ft_' and named to mirror the function it replicates.

| header   | 0 | 1 | 2 | 3 |
| -------- | -------- | --------- | -------- | -------- |
|ctype.h|[isalpha](./ft_isalpha.c)|isalnum|isascii|isprint|toupper|tolower|

| header   | 0 |
| -------- | -------- |
|strings.h|bzero|

| header   | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 |
| -------- | -------- | --------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- |
|string.h|strlen|memset| memcpy|memmove|strlcpy|strlcat|strchr|strncmp|memchr|memcmp|strnstr|strdup

| header   | 0 | 1 |
| -------- | -------- | --------- |
|stdlib.h|atoi|calloc|
