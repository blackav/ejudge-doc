Навигация: [Система ejudge](Система_ejudge "wikilink")/[Проверяющие
программы](Проверяющие_программы "wikilink")/[libchecker](libchecker "wikilink")/[Функции](Libchecker:Функции "wikilink")/[Завершение
работы](Libchecker:Завершение_работы "wikilink")/[fatal](Libchecker:fatal "wikilink")

`void fatal(int code, char const *format, ...);`

Данная функция печатает на стандартный поток ошибок сообщение в
соответствии со спецификацией формата format для функции printf и
дополнительными аргументами, затем печатается символ перехода на новую
строку, затем выполнение проверяющей программы завершается с кодом
возврата code. Данная функция никогда не возвращает управление в
проверяющую программу. В качестве значения параметра code рекомендуется
использовать константы RUN_OK, RUN_PRESENTATION_ERR,
RUN_WRONG_ANSWER_ERR или RUN_CHECK_FAILED.

Для завершения проверяющей программы с соответствующим кодом ошибки
рекомендуется применять функции
[fatal_CF](libchecker:fatal_CF "wikilink"),
[fatal_PE](libchecker:fatal_PE "wikilink"),
[fatal_WA](libchecker:fatal_WA "wikilink"),
[fatal_read](libchecker:fatal_read "wikilink").
