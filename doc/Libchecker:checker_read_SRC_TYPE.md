Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Проверяющие
программы](Проверяющие_программы "wikilink")/[libchecker](libchecker "wikilink")/[Функции](Libchecker:Функции "wikilink")/[Чтение
целых значений](Libchecker:Чтение_целых_значений "wikilink")/[Чтение
целого значения из файла](Libchecker:checker_read_SRC_TYPE "wikilink")

Данные функции позволяют считывать целое значение из файла указываемого
в имени функции.

`int checker_read_in_int(const char *name, int eof_error_flag, int *p_val);`  
`int checker_read_out_int(const char *name, int eof_error_flag, int *p_val);`  
`int checker_read_corr_int(const char *name, int eof_error_flag, int *p_val);`  
`int checker_read_in_unsigned_int(const char *name, int eof_error_flag, unsigned int *p_val);`  
`int checker_read_out_unsigned_int(const char *name, int eof_error_flag, unsigned int *p_val);`  
`int checker_read_corr_unsigned_int(const char *name, int eof_error_flag, unsigned int *p_val);`  
`int checker_read_in_long_long(const char *name, int eof_error_flag, long long *p_val);`  
`int checker_read_out_long_long(const char *name, int eof_error_flag, long long *p_val);`  
`int checker_read_corr_long_long(const char *name, int eof_error_flag, long long *p_val);`  
`int checker_read_in_unsigned_long_long(const char *name, int eof_error_flag, unsigned long long *p_val);`  
`int checker_read_out_unsigned_long_long(const char *name, int eof_error_flag, unsigned long long *p_val);`  
`int checker_read_corr_unsigned_long_long(const char *name, int eof_error_flag, unsigned long long *p_val);`

Здесь `_in_` в имени функции означает, что чтение ведется из входного
файла, `_out_` — чтение ведется из файла с результатом работы
тестируемой программы, `_corr_` — чтение ведется из файла с правильным
ответом.

Параметр `name` — это строка или текст, описывающий считываемое
значение. Он используется в случае ошибки при выводе диагностических
сообщений. Параметр `eof_error_flag` задает поведение функции в случае,
если достигнут конец файла. Если параметр имеет ненулевое значение, то в
случае невозможности чтения числа из-за достижения конца файла
диагностируется [ошибка неправильного формата
файла](ошибка_неправильного_формата_файла "wikilink"). Если параметр
`eof_error_flag` равен 0, то в случае достижения конца файла
возвращается значение -1. Параметр `p_val` — это адрес переменной, в
которую должно быть помещено считанное значение.

Число в файле должно быть записано в десятичном виде с необязательными
знаками + или - перед ним. Перед числом пропускаются [пробельные
символы](пробельный_символ "wikilink"). Если нарушен формат записи числа
или число выходит за диапазон представимых значений заданного типа,
диагностируется [ошибка неправильного формата
файла](ошибка_неправильного_формата_файла "wikilink").

Функция возвращает значение 1 при успешном чтении и -1 при достижении
конца файла, если параметр `eof_error_flag` равен 0. В случае
возникновения ошибки чтения данных, управление в вызывающую функцию не
возвращается.
