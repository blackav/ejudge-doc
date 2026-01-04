Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Конфигурационные
параметры
задач](serve.cfg:problem.md)/[disable_ctrl_chars](serve.cfg:problem:disable_ctrl_chars.md)

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Abstract problems"*, поле *"Disable any
control characters in the source code"*, либо страница *"Editing
contest"*, вкладка *"Problems (serve.cfg)"*, блок *"Concrete problems"*,
поле *"Disable any control characters in the source code"*.

Если данная переменная установлена в 1, при сдаче текстов программ
запрещается использование управляющих символов, кроме `\r` и `\n`. В
частности, запрещается использование `\t`.
