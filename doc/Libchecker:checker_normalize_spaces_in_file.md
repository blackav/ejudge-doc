Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Проверяющие
программы](Проверяющие_программы "wikilink")/[libchecker](libchecker "wikilink")/[Функции](Libchecker:Функции "wikilink")/[Чтение
файла как
текста](Libchecker:Чтение_файла_как_текста "wikilink")/[checker_normalize_spaces_in_file](Libchecker:checker_normalize_spaces_in_file "wikilink")

Функция `checker_normalize_file` — удалить повторяющиеся пробельные
символы из считанного в память [текстового
файла](текстовый_файл "wikilink").

`void checker_normalize_spaces_in_file(char **lines, size_t *lines_num);`

Функция удаляет [пробельные символы](пробельный_символ "wikilink"),
находящиеся в началах и на концах строк. Последовательность из
нескольких пробельных символов в середине строки заменяется на один
символ пробела. Затем удаляются пустые строки. Параметр `lines` — это
указатель на массив указателей на строки текста, считанного из файла в
память. Указатели на строки текста не могут быть равны NULL. Параметр
`lines_num` — это указатель на переменную, которая хранит количество
считанных из файла строк текста. В результате работы функции значение
этой переменной может измениться.

См. также:
[checker_normalize_file](libchecker:checker_normalize_file "wikilink"),[checker_read_file_by_line](libchecker:checker_read_file_by_line "wikilink"),
[checker_read_file_by_line_f](libchecker:checker_read_file_by_line_f "wikilink").
