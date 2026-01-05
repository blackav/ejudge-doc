Навигация: [Главная страница](../main_Page.md)/[Система
ejudge](../система_ejudge.md)/[Проверяющие
программы](../проверяющие_программы.md)/[libchecker](../libchecker.md)/[Функции](../функции.md)/[Чтение
файла как
текста](Чтение_файла_как_текста.md)/[checker_normalize_file](checker_normalize_file.md)

Функция `checker_normalize_file` — удалить незначащие пробелы из
считанного в память [текстового файла](../текстовый_файл.md).

`void checker_normalize_file(char **lines, size_t *lines_num);`

Функция удаляет [пробельные символы](../пробельный_символ.md),
находящиеся на концах строк. Затем удаляются пустые строки в конце
массива строк. Параметр `lines` — это указатель на массив указателей на
строки текста, считанного из файла в память. Указатели на строки текста
не могут быть равны NULL. Параметр `lines_num` — это указатель на
переменную, которая хранит количество считанных из файла строк текста. В
результате работы функции значение этой переменной может измениться.

См. также:
[checker_normalize_spaces_in_file](checker_normalize_spaces_in_file.md),[checker_read_file_by_line](checker_read_file_by_line.md),
[checker_read_file_by_line_f](checker_read_file_by_line_f.md).
