Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[`max_user_run_count`](serve.cfg:problem:max_user_run_count "wikilink")

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Abstract problems"*, поле *"Max
submissions for the problem"*, либо страница *"Editing contest"*,
вкладка *"Problems (serve.cfg)"*, блок *"Concrete problems"*, поле *"Max
submissions for the problem"*.

Данная конфигурационная переменная позволяет задать максимальное число
сдач решений по данной задаче. Например,

`max_user_run_count = 5`

задает, что по данной задаче допускается не более 5 попыток. Попытки со
статусом [Ignored](Ignored "wikilink") не учитываются при подсчете числа
попыток. Попытки со статусом [Compilation
Error](Compilation_Error "wikilink") не учитываются, если установлена
переменная
[`ignore_compile_errors`](serve.cfg:problem:ignore_compile_errors "wikilink").
