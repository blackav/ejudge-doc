Навигация: [Главная страница](../../main_Page.md)/[Система
ejudge](../../система_ejudge.md)/[Использование](../../использование.md)/[Конфигурационные
файлы](../../конфигурационные_файлы.md)/[serve.cfg](../../serve.cfg.md)/[Конфигурационные
параметры
задач](../problem.md)/[`max_user_run_count`](max_user_run_count.md)

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Abstract problems"*, поле *"Max
submissions for the problem"*, либо страница *"Editing contest"*,
вкладка *"Problems (serve.cfg)"*, блок *"Concrete problems"*, поле *"Max
submissions for the problem"*.

Данная конфигурационная переменная позволяет задать максимальное число
сдач решений по данной задаче. Например,

`max_user_run_count = 5`

задает, что по данной задаче допускается не более 5 попыток. Попытки со
статусом [Ignored](../../ignored.md) не учитываются при подсчете числа
попыток. Попытки со статусом [Compilation
Error](../../compilation_Error.md) не учитываются, если установлена
переменная
[`ignore_compile_errors`](ignore_compile_errors.md).
