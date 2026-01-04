Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Проверяющие
программы](Проверяющие_программы "wikilink")/[libchecker](libchecker "wikilink")/[Типы
данных](libchecker:Типы_данных "wikilink")/[checker_error_func_t](libchecker:checker_error_func_t "wikilink")

`typedef void (*checker_error_func_t)(char const *format, ...)`  
`         LIBCHECKER_ATTRIB((noreturn, format(printf, 1, 2)));`

Этот тип данных определяет указатель на функцию, которая вызывается в
случае ошибки при чтении данных. Функция не должна возвращать управление
в вызвавшую ее функцию, а параметр `format` — это строка, которая
передается функции семейства `printf`.

Функции [`fatal_CF`](libchecker:fatal_CF "wikilink"),
[`fatal_PE`](libchecker:fatal_PE "wikilink"),
[`fatal_WA`](libchecker:fatal_WA "wikilink") совместимы с типом
`checker_error_func_t`, поэтому могут передаваться в качестве аргументов
в функции, которые требуют функцию для вывода сообщений об ошибке.
