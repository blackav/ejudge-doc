Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Проверяющие
программы](Проверяющие_программы.md)/[libchecker](libchecker.md)/[Типы
данных](libchecker:Типы_данных.md)/[checker_error_func_t](libchecker:checker_error_func_t.md)

`typedef void (*checker_error_func_t)(char const *format, ...)`  
`         LIBCHECKER_ATTRIB((noreturn, format(printf, 1, 2)));`

Этот тип данных определяет указатель на функцию, которая вызывается в
случае ошибки при чтении данных. Функция не должна возвращать управление
в вызвавшую ее функцию, а параметр `format` — это строка, которая
передается функции семейства `printf`.

Функции [`fatal_CF`](libchecker:fatal_CF.md),
[`fatal_PE`](libchecker:fatal_PE.md),
[`fatal_WA`](libchecker:fatal_WA.md) совместимы с типом
`checker_error_func_t`, поэтому могут передаваться в качестве аргументов
в функции, которые требуют функцию для вывода сообщений об ошибке.
