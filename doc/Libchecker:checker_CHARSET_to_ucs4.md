Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Проверяющие
программы](Проверяющие_программы "wikilink")/[libchecker](libchecker "wikilink")/[Функции](Libchecker:Функции "wikilink")/[Перекодирование
текстовых
данных](Libchecker:Перекодирование_текстовых_данных "wikilink")/[Перекодирование
одного символа в кодировку
UCS-4](Libchecker:checker_CHARSET_to_ucs4 "wikilink")

Данные функции позволяют перекодировать один символ из нескольких
поддерживаемых однобайтных кириллических кодировок в кодировку UCS-4.

`int checker_koi8r_to_ucs4(int c);`  
`int checker_cp866_to_ucs4(int c);`  
`int checker_cp1251_to_ucs4(int c);`  
`int checker_iso_to_ucs4(int c);`  
`int checker_mac_to_ucs4(int c);`

Параметр `c` — это код символа в соответствующей кириллической
кодировке. Функция возвращает соответствующий код в кодировке UCS-4.
