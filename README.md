# string_lib
*Project for School 21*
___
My implementation of the standard string.h library in the C programming language 



![string](https://github.com/ArzimanOff/my_string_h_lib/assets/102418559/dbdd29f9-ceea-4ac9-afd9-c424007d0f12)

## Руководство по использованию (◕‿◕)

### Для сборки библиотеки и исполняемого файла тестов, используй следующие команды:

```make all```

### Для запуска тестов и проверки утечек памяти:

```make leaks```

### Для создания отчета о покрытии кода:

```make gcov_report```

### Для применения стиля форматирования Google к коду:

```make style```

### string.h Типы

| № | Переменная | Описание |
| ------ | ------ | ------ |
| 1 | size_t | Целочисленный тип без знака, являющийся результатом ключевого слова sizeof.
	
### string.h Макросы

| № | Макрос | Описание |
| ------ | ------ | ------ |
| 1 | NULL | Макрос, являющийся значением константы нулевого указателя.

### string.h Функции

| № | Функция | Описание |
| ------ | ------ | ------ |
| 1 | void *memchr(const void *str, int c, size_t n) | Выполняет поиск первого вхождения символа c (беззнаковый тип) в первых n байтах строки, на которую указывает аргумент str. |
| 2 | int memcmp(const void *str1, const void *str2, size_t n) | Сравнивает первые n байтов str1 и str2. |
| 3 | void *memcpy(void *dest, const void *src, size_t n) | Копирует n символов из src в dest. |
| 4 | void *memset(void *str, int c, size_t n) | Копирует символ c (беззнаковый тип) в первые n символов строки, на которую указывает аргумент str. |
| 5 | char *strncat(char *dest, const char *src, size_t n) | Добавляет строку, на которую указывает src, в конец строки, на которую указывает dest, длиной до n символов. |
| 6	| char *strchr(const char *str, int c) | Выполняет поиск первого вхождения символа c (беззнаковый тип) в строке, на которую указывает аргумент str. |
| 7 | int strncmp(const char *str1, const char *str2, size_t n) | Сравнивает не более первых n байтов str1 и str2. |
| 8 | char *strncpy(char *dest, const char *src, size_t n) | Копирует до n символов из строки, на которую указывает src, в dest. |
| 9 | size_t strcspn(const char *str1, const char *str2) | Вычисляет длину начального сегмента str1, который полностью состоит из символов, не входящих в str2. |
| 10 | char *strerror(int errnum) | Выполняет поиск во внутреннем массиве номера ошибки errnum и возвращает указатель на строку с сообщением об ошибке. Нужно объявить макросы, содержащие массивы сообщений об ошибке для операционных систем mac и linux. Описания ошибок есть в оригинальной библиотеке. Проверка текущей ОС осуществляется с помощью директив.|
| 11 | size_t strlen(const char *str) | Вычисляет длину строки str, не включая завершающий нулевой символ. |
| 12 | char *strpbrk(const char *str1, const char *str2) | Находит первый символ в строке str1, который соответствует любому символу, указанному в str2. |
| 13 | char *strrchr(const char *str, int c) | Выполняет поиск последнего вхождения символа c (беззнаковый тип) в строке, на которую указывает аргумент str. |
| 14 | char *strstr(const char *haystack, const char *needle) | Находит первое вхождение всей строки needle (не включая завершающий нулевой символ), которая появляется в строке haystack. |
| 15 | char *strtok(char *str, const char *delim) | Разбивает строку str на ряд токенов, разделенных delim. |



### Специальные функции обработки строк (вдохновленные классом String в языке C#)

| № | Функция | Описание |
| ------ | ------ | ------ |
| 1 | void *to_upper(const char *str) | Возвращает копию строки (str), преобразованной в верхний регистр. В случае какой-либо ошибки следует вернуть значение NULL |
| 2 | void *to_lower(const char *str) | Возвращает копию строки (str), преобразованной в нижний регистр. В случае какой-либо ошибки следует вернуть значение NULL |
| 3 | void *insert(const char *src, const char *str, size_t start_index) | Возвращает новую строку, в которой указанная строка (str) вставлена в указанную позицию (start_index) в данной строке (src). В случае какой-либо ошибки следует вернуть значение NULL |
| 4 | void *trim(const char *src, const char *trim_chars) | Возвращает новую строку, в которой удаляются все начальные и конечные вхождения набора заданных символов (trim_chars) из данной строки (src). В случае какой-либо ошибки следует вернуть значение NULL |

