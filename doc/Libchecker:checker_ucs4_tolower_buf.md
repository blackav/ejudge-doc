Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Проверяющие
программы](Проверяющие_программы "wikilink")/[libchecker](libchecker "wikilink")/[Функции](Libchecker:Функции "wikilink")/[Перекодирование
текстовых
данных](Libchecker:Перекодирование_текстовых_данных "wikilink")\|[checker_ucs4_tolower_buf](Libchecker:checker_ucs4_tolower_buf "wikilink")

Функция перекодироует символы из заданного UCS-4 буфера в нижний
регистр.

`int *checker_ucs4_tolower_buf(int *buf, size_t size);`

Параметр `buf` — адрес буфера для перекодирования, параметр `size` — его
размер. Параметр `buf` не может быть равен `NULL`. Перекодирование
ведется непосредственно в буфере.

Функция возвращает значение параметра `buf`.

См. также:
[`checker_ucs4_tolower`](libchecker:checker_ucs4_tolower "wikilink"),
[`checker_ucs4_tolower_str`](libchecker:checker_ucs4_tolower_str "wikilink").
