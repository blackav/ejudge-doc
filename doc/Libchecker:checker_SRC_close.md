Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Проверяющие
программы](Проверяющие_программы "wikilink")/[libchecker](libchecker "wikilink")/[Функции](Libchecker:Функции "wikilink")/[Работа
с потоками
ввода-вывода](Libchecker:Работа_с_потоками_ввода_вывода "wikilink")/[Закрытие
файла](Libchecker:checker_SRC_close "wikilink")

Функции позволяют закрыть файл.

`void checker_in_close(void);`  
`void checker_out_close(void);`  
`void checker_corr_close(void);`

Здесь `_in_` в имени функции означает входной файл, `_out_` — файл с
результатом работы тестируемой программы, `_corr_` — файл с правильным
ответом.

Функции закрывают соответствующий файл. Если при закрытии файла
возникает ошибка ввода, диагностируется [внутренняя ошибка
проверки](внутренняя_ошибка_проверки "wikilink"). В этом случае
вызывается функция [`fatal_CF`](Libchecker:fatal_CF "wikilink").
