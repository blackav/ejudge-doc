Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Проверяющие
программы](Проверяющие_программы "wikilink")/[libchecker](libchecker "wikilink")/[Функции](Libchecker:Функции "wikilink")/[Перекодирование
текстовых
данных](Libchecker:Перекодирование_текстовых_данных "wikilink")\|[checker_ucs4_tolower_str](Libchecker:checker_ucs4_tolower_str "wikilink")

Функция перекодироует символы в заданной UCS-4 строке в нижний регистр.

`int *checker_ucs4_tolower_buf(int *str);`

Параметр `str` — адрес строки для перекодирования. Параметр `str` не
может быть равен `NULL`, строка должна завершаться символом с кодом 0.
Перекодирование ведется непосредственно в строке.

Функция возвращает значение параметра `str`.

См. также:
[`checker_ucs4_tolower`](libchecker:checker_ucs4_tolower "wikilink"),
[`checker_ucs4_tolower_buf`](libchecker:checker_ucs4_tolower_buf "wikilink").
