Навигация: [Главная страница](../main_Page.md)/[Система
ejudge](../система_ejudge.md)/[Проверяющие
программы](../проверяющие_программы.md)/[libchecker](../libchecker.md)/[Функции](../функции.md)/[Перекодирование
текстовых
данных](Перекодирование_текстовых_данных.md)/[Перекодирование
буфера в кодировку
UCS-4](checker_CHARSET_to_ucs4_buf.md)

Данные функции позволяют перекодировать символьный буфер из одной из
поддерживаемых однобайтных кириллических кодировок в кодировку UCS-4.

`int checker_koi8r_to_ucs4_buf(int *out_buf, const char *in_buf, size_t in_size);`  
`int checker_cp866_to_ucs4_buf(int *out_buf, const char *in_buf, size_t in_size);`  
`int checker_cp1251_to_ucs4_buf(int *out_buf, const char *in_buf, size_t in_size);`  
`int checker_iso_to_ucs4_buf(int *out_buf, const char *in_buf, size_t in_size);`  
`int checker_mac_to_ucs4_buf(int *out_buf, const char *in_buf, size_t in_size);`

Данные функции перекодируют символьный буфер, расположенный по адресу
`in_buf` и содержащий `in_size` байт, в выходной буфер, расположенный по
адресу `out_buf`. Буфер `out_buf` должен иметь достаточный размер, чтобы
разместить все символы входного буфера. Другими словами, размер буфера
`out_buf` должен быть как минимум `in_size`. Ни параметр `in_buf`, ни
параметр `out_buf` не могут быть равны `NULL`. Нулевой байт во входном
буфере перекодируется в нулевое значение в выходном буфере.

Функция возвращает количество перекодированных символов, то есть
`in_size`.
