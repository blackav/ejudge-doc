Навигация: [Главная страница](../main_Page.md)/[Система
ejudge](../система_ejudge.md)/[Проверяющие
программы](../проверяющие_программы.md)/[libchecker](../libchecker.md)/[Функции](../функции.md)/[Перекодирование
текстовых
данных](Перекодирование_текстовых_данных.md)\|[checker_ucs4_tolower_buf](checker_ucs4_tolower_buf.md)

Функция перекодироует символы из заданного UCS-4 буфера в нижний
регистр.

`int *checker_ucs4_tolower_buf(int *buf, size_t size);`

Параметр `buf` — адрес буфера для перекодирования, параметр `size` — его
размер. Параметр `buf` не может быть равен `NULL`. Перекодирование
ведется непосредственно в буфере.

Функция возвращает значение параметра `buf`.

См. также:
[`checker_ucs4_tolower`](checker_ucs4_tolower.md),
[`checker_ucs4_tolower_str`](checker_ucs4_tolower_str.md).
