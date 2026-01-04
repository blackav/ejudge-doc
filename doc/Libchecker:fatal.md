Навигация: [Система ejudge](Система_ejudge.md)/[Проверяющие
программы](Проверяющие_программы.md)/[libchecker](libchecker.md)/[Функции](Libchecker:Функции.md)/[Завершение
работы](Libchecker:Завершение_работы.md)/[fatal](Libchecker:fatal.md)

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
[fatal_CF](libchecker:fatal_CF.md),
[fatal_PE](libchecker:fatal_PE.md),
[fatal_WA](libchecker:fatal_WA.md),
[fatal_read](libchecker:fatal_read.md).
