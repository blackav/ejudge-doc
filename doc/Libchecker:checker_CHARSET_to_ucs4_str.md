Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Проверяющие
программы](Проверяющие_программы "wikilink")/[libchecker](libchecker "wikilink")/[Функции](Libchecker:Функции "wikilink")/[Перекодирование
текстовых
данных](Libchecker:Перекодирование_текстовых_данных "wikilink")/[Перекодирование
строки в кодировку
UCS-4](Libchecker:checker_CHARSET_to_ucs4_str "wikilink")

Данные функции позволяют перекодировать строку, завершающуюся нулевым
байтом, в одной из поддерживаемых кириллических кодировок в кодировку
UCS-4.

`int checker_koi8r_to_ucs4_str(int *out_buf, const char *str);`  
`int checker_cp866_to_ucs4_str(int *out_buf, const char *str);`  
`int checker_cp1251_to_ucs4_str(int *out_buf, const char *str);`  
`int checker_iso_to_ucs4_str(int *out_buf, const char *str);`  
`int checker_mac_to_ucs4_str(int *out_buf, const char *str);`

Параметр `str` — перекодируемая строка. Параметр не может быть равен
`NULL`. Параметр `out_buf` — адрес буфера, в котором будет сохранениа
перекодированная строка. Параметр не может быть равен `NULL`. Буфер
`out_buf` должен иметь достаточный размер для размещения
перекодированных символов и кода завершения строки 0, то есть иметь
размер не меньше, чем `strlen(str) + 1`.

Функции возвращают число перекодированных символов без учета
завершающего нулевого символа, то есть значение `strlen(str)`.
