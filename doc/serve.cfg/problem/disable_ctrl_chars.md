Навигация: [Главная страница](../../main_Page.md)/[Система
ejudge](../../система_ejudge.md)/[Использование](../../использование.md)/[Конфигурационные
файлы](../../конфигурационные_файлы.md)/[serve.cfg](../../serve.cfg.md)/[Конфигурационные
параметры
задач](../problem.md)/[disable_ctrl_chars](disable_ctrl_chars.md)

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Abstract problems"*, поле *"Disable any
control characters in the source code"*, либо страница *"Editing
contest"*, вкладка *"Problems (serve.cfg)"*, блок *"Concrete problems"*,
поле *"Disable any control characters in the source code"*.

Если данная переменная установлена в 1, при сдаче текстов программ
запрещается использование управляющих символов, кроме `\r` и `\n`. В
частности, запрещается использование `\t`.
