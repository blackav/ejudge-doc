Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Проверяющие
программы](Проверяющие_программы.md)/[libchecker](libchecker.md)/[Функции](Libchecker:Функции.md)/[Перекодирование
текстовых
данных](Libchecker:Перекодирование_текстовых_данных.md)

Если в задаче требуется вывести текст на русском языке, при проверке
вывода возникает проблема множественности кириллических кодировок. В
зависимости от операционной системы, ее настроек или среды
программирования, в которой подготовленна программа, русский текст может
быть представлен в одной из следующих кодировок:
[KOI8-R](http://ru.wikipedia.org/wiki/KOI8-R),
[CP1251](http://ru.wikipedia.org/wiki/Windows-1251),
[CP866](http://ru.wikipedia.org/wiki/CP866),
[ISO](http://ru.wikipedia.org/wiki/ISO8859-5),
[MAC](http://ru.wikipedia.org/wiki/MacCyrillic),
[UTF-8](http://ru.wikipedia.org/wiki/UTF-8).

В качестве внутренней кодировки при обработке кириллических данных в
библиотеке libchecker используется кодировка
[UCS-4](http://ru.wikipedia.org/wiki/UCS-4), в которой на один символ
отводится 4 байта. Библиотека предоставляет функции перекодирования
данных в кодировку UCS-4 и обработки.

|                                                                                          |                                                                                                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [`checker_koi8r_to_ucs4`](Libchecker:checker_CHARSET_to_ucs4.md)                 | перекодировать один символ из кодировки KOI8-R в кодировку UCS-4                                                                   |
| [`checker_cp866_to_ucs4`](Libchecker:checker_CHARSET_to_ucs4.md)                 | перекодировать один символ из кодировки CP866 в кодировку UCS-4                                                                    |
| [`checker_cp1251_to_ucs4`](Libchecker:checker_CHARSET_to_ucs4.md)                | перекодировать один символ из кодировки CP1251 в кодировку UCS-4                                                                   |
| [`checker_koi8r_to_ucs4_buf`](Libchecker:checker_CHARSET_to_ucs4_buf.md)         | перекодировать буфер заданного размера из кодировки KOI8-R в кодировку UCS-4                                                       |
| [`checker_cp866_to_ucs4_buf`](Libchecker:checker_CHARSET_to_ucs4_buf.md)         | перекодировать буфер заданного размера из кодировки CP866 в кодировку UCS-4                                                        |
| [`checker_cp1251_to_ucs4_buf`](Libchecker:checker_CHARSET_to_ucs4_buf.md)        | перекодировать буфер заданного размера из кодировки CP1251 в кодировку UCS-4                                                       |
| [`checker_koi8r_to_ucs4_str`](Libchecker:checker_CHARSET_to_ucs4_str.md)         | перекодировать строку из кодировки KOI8-R в кодировку UCS-4                                                                        |
| [`checker_cp866_to_ucs4_str`](Libchecker:checker_CHARSET_to_ucs4_str.md)         | перекодировать строку из кодировки CP866 в кодировку UCS-4                                                                         |
| [`checker_cp1251_to_ucs4_str`](Libchecker:checker_CHARSET_to_ucs4_str.md)        | перекодировать строку из кодировки CP1251 в кодировку UCS-4                                                                        |
| [`checker_utf8_to_ucs4_buf`](Libchecker:checker_utf8_to_ucs4_buf.md)             | перекодировать буфер заданного размера из кодировки UTF-8 в кодировку UCS-4                                                        |
| [`checker_utf8_to_ucs4_str`](Libchecker:checker_utf8_to_ucs4_str.md)             | перекодировать строку из кодировки UTF-8 в кодировку UCS-4                                                                         |
| [`checker_ucs4_to_koi8r`](Libchecker:checker_ucs4_to_CHARSET.md)                 | перекодировать один символ из кодировки UCS-4 в кодировку KOI8-R                                                                   |
| [`checker_ucs4_to_koi8r_str`](Libchecker:checker_ucs4_to_CHARSET_str.md)         | перекодировать строку из кодировки UCS-4 в кодировку KOI8-R                                                                        |
| [`checker_ucs4_to_utf8_size`](Libchecker:checker_ucs4_to_utf8_size.md)           | рассчитать число байт необходимых для кодирования заданной UCS-4 строки в кодировку UTF-8                                          |
| [`checker_ucs4_to_utf8_str`](Libchecker:checker_ucs4_to_utf8_str.md)             | перекодировать строку из кодировки UCS-4 в кодировку UTF-8                                                                         |
| [`checker_ucs4_tolower`](Libchecker:checker_ucs4_tolower.md)                     | перевести символ в кодировке UCS-4 в нижний регистр                                                                                |
| [`checker_ucs4_tolower_buf`](Libchecker:checker_ucs4_tolower_buf.md)             | перевести буфер заданного размера в кодировке UCS-4 в нижний регистр                                                               |
| [`checker_ucs4_tolower_str`](Libchecker:checker_ucs4_tolower_str.md)             | перевести строку в кодировке UCS-4 в нижний регистр                                                                                |
| [`checker_strcmp_ucs4`](Libchecker:checker_strcmp_ucs4.md)                       | сравнить две UCS-4 строки                                                                                                          |
| [`checker_eq_str_rus_ucs4`](Libchecker:checker_eq_str_rus_ucs4.md)               | проверить совпадение строки в одной из поддерживаемых кириллических кодировок со строкой в кодировке UCS-4                         |
| [`checker_eq_str_rus_ucs4_nocase`](Libchecker:checker_eq_str_rus_ucs4_nocase.md) | проверить совпадение строки в одной из поддерживаемых кириллических кодировок со строкой в кодировке UCS-4 без учета регистра букв |
| [`checker_is_utf8_locale`](Libchecker:checker_is_utf8_locale.md)                 | проверить, что проверяющая программа работает в UTF-8 локали                                                                       |
