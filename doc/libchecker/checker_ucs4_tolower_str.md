Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Проверяющие
программы](Проверяющие_программы.md)/[libchecker](libchecker.md)/[Функции](Libchecker:Функции.md)/[Перекодирование
текстовых
данных](Libchecker:Перекодирование_текстовых_данных.md)\|[checker_ucs4_tolower_str](Libchecker:checker_ucs4_tolower_str.md)

Функция перекодироует символы в заданной UCS-4 строке в нижний регистр.

`int *checker_ucs4_tolower_buf(int *str);`

Параметр `str` — адрес строки для перекодирования. Параметр `str` не
может быть равен `NULL`, строка должна завершаться символом с кодом 0.
Перекодирование ведется непосредственно в строке.

Функция возвращает значение параметра `str`.

См. также:
[`checker_ucs4_tolower`](libchecker:checker_ucs4_tolower.md),
[`checker_ucs4_tolower_buf`](libchecker:checker_ucs4_tolower_buf.md).
