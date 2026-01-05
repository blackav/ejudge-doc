Навигация: [Главная страница](../main_Page.md)/[Система
ejudge](../система_ejudge.md)/[Проверяющие
программы](../проверяющие_программы.md)/[libchecker](../libchecker.md)/[Функции](../функции.md)/[Чтение
целых значений](Чтение_целых_значений.md)/[Чтение
целого значения из файла](checker_read_SRC_TYPE.md)

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
файла](../ошибка_неправильного_формата_файла.md). Если параметр
`eof_error_flag` равен 0, то в случае достижения конца файла
возвращается значение -1. Параметр `p_val` — это адрес переменной, в
которую должно быть помещено считанное значение.

Число в файле должно быть записано в десятичном виде с необязательными
знаками + или - перед ним. Перед числом пропускаются [пробельные
символы](../пробельный_символ.md). Если нарушен формат записи числа
или число выходит за диапазон представимых значений заданного типа,
диагностируется [ошибка неправильного формата
файла](../ошибка_неправильного_формата_файла.md).

Функция возвращает значение 1 при успешном чтении и -1 при достижении
конца файла, если параметр `eof_error_flag` равен 0. В случае
возникновения ошибки чтения данных, управление в вызывающую функцию не
возвращается.
