# string_lib
*Project for School 21*
___
My implementation of the standard string.h library in the C programming language 



![string](https://github.com/ArzimanOff/my_string_h_lib/assets/102418559/dbdd29f9-ceea-4ac9-afd9-c424007d0f12)

## Usage guide

### To build the library and test executable, use the following commands:

```make all```

### To run tests and check for memory leaks:

```make leaks```

### To create a code coverage report:

```make gcov_report```

### To apply Google's formatting style to the code:

```make style```

### string.h Types

| № | Variable | Description |
| ------ | ------ | ------ |
| 1 | size_t | An unsigned integer type that is the result of the sizeof keyword.
	
### string.h Macros

| № | Macros | Description |
| ------ | ------ | ------ |
| 1 | NULL | A macro that is the value of a null pointer constant.

### string.h Functions

| № | Function | Description |
| ------ | ------ | ------ |
| 1 | void *memchr(const void *str, int c, size_t n) | Searches for the first occurrence of the character c (unsigned type) in the first n bytes of the string pointed to by the str argument. |
| 2 | int memcmp(const void *str1, const void *str2, size_t n) | Compares the first n bytes of str1 and str2. |
| 3 | void *memcpy(void *dest, const void *src, size_t n) | Copies n characters from src to dest. |
| 4 | void *memset(void *str, int c, size_t n) | Copies the character c (unsigned type) into the first n characters of the string pointed to by the str argument. |
| 5 | char *strncat(char *dest, const char *src, size_t n) | Adds the string pointed to by src to the end of the string pointed to by dest, up to n characters long. |
| 6	| char *strchr(const char *str, int c) | Searches for the first occurrence of the character c (unsigned type) in the string pointed to by the str argument. |
| 7 | int strncmp(const char *str1, const char *str2, size_t n) | Compares at most the first n bytes of str1 and str2. |
| 8 | char *strncpy(char *dest, const char *src, size_t n) | Copies up to n characters from the string pointed to by src to dest. |
| 9 | size_t strcspn(const char *str1, const char *str2) | Calculates the length of the initial segment of str1, which consists entirely of characters not included in str2. |
| 10 | char *strerror(int errnum) | Searches the internal array for errnum error number and returns a pointer to the error message string. We need to declare macros containing arrays of error messages for mac and linux operating systems. The error descriptions are in the original library. The current operating system is checked using directives.|
| 11 | size_t strlen(const char *str) | Calculates the length of the string str, not including the terminating null character. |
| 12 | char *strpbrk(const char *str1, const char *str2) | Finds the first character in str1 that matches any character specified in str2. |
| 13 | char *strrchr(const char *str, int c) | Searches for the last occurrence of the character c (unsigned type) in the string pointed to by the str argument. |
| 14 | char *strstr(const char *haystack, const char *needle) | Finds the first occurrence of the entire needle string (not including the terminating null character) that appears in the haystack string. |
| 15 | char *strtok(char *str, const char *delim) | Splits the string str into a number of tokens separated by delim. |



### Special string processing functions (inspired by the String class in C#)

| № | Function | Description |
| ------ | ------ | ------ |
| 1 | void *to_upper(const char *str) | Returns a copy of the string (str) converted to uppercase. In case of any error, return NULL |
| 2 | void *to_lower(const char *str) | Returns a copy of the string (str) converted to lower case. In case of any error, return NULL |
| 3 | void *insert(const char *src, const char *str, size_t start_index) | Returns a new line in which the specified string (str) is inserted at the specified position (start_index) in the given line (src). In case of any error, return NULL |
| 4 | void *trim(const char *src, const char *trim_chars) | Returns a new string that removes all start and end occurrences of a set of specified characters (trim_chars) from the given string (src). In case of any error, return NULL |

