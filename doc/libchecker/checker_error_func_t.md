Навигация: [Главная страница](../main_Page.md)/[Система
ejudge](../система_ejudge.md)/[Проверяющие
программы](../проверяющие_программы.md)/[libchecker](../libchecker.md)/[Типы
данных](libchecker:Типы_данных.md)/[checker_error_func_t](checker_error_func_t.md)

`typedef void (*checker_error_func_t)(char const *format, ...)`  
`         LIBCHECKER_ATTRIB((noreturn, format(printf, 1, 2)));`

Этот тип данных определяет указатель на функцию, которая вызывается в
случае ошибки при чтении данных. Функция не должна возвращать управление
в вызвавшую ее функцию, а параметр `format` — это строка, которая
передается функции семейства `printf`.

Функции [`fatal_CF`](fatal_CF.md),
[`fatal_PE`](fatal_PE.md),
[`fatal_WA`](fatal_WA.md) совместимы с типом
`checker_error_func_t`, поэтому могут передаваться в качестве аргументов
в функции, которые требуют функцию для вывода сообщений об ошибке.
