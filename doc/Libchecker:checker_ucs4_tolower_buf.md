Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Проверяющие
программы](Проверяющие_программы.md)/[libchecker](libchecker.md)/[Функции](Libchecker:Функции.md)/[Перекодирование
текстовых
данных](Libchecker:Перекодирование_текстовых_данных.md)\|[checker_ucs4_tolower_buf](Libchecker:checker_ucs4_tolower_buf.md)

Функция перекодироует символы из заданного UCS-4 буфера в нижний
регистр.

`int *checker_ucs4_tolower_buf(int *buf, size_t size);`

Параметр `buf` — адрес буфера для перекодирования, параметр `size` — его
размер. Параметр `buf` не может быть равен `NULL`. Перекодирование
ведется непосредственно в буфере.

Функция возвращает значение параметра `buf`.

См. также:
[`checker_ucs4_tolower`](libchecker:checker_ucs4_tolower.md),
[`checker_ucs4_tolower_str`](libchecker:checker_ucs4_tolower_str.md).
