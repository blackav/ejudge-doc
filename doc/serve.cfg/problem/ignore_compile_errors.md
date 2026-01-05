Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Конфигурационные
параметры
задач](serve.cfg:problem.md)/[ignore_compile_errors](serve.cfg:problem:ignore_compile_errors.md)

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Abstract problems"*, поле *"Ignore
compilation errors"*, либо страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Concrete problems"*, поле *"Ignore
compilation errors"*.

Эта переменная позволяет переопределить действие глобальной
конфигурационной переменной
[`ignore_compile_errors`](serve.cfg:global:ignore_compile_errors.md)
для одной задачи. Например, если глобальная переменная установлена (то
есть ошибки компиляции игнорируются при подсчёте результатов), строка

`ignore_compile_errors = 0`

раздела определения задачи позволит не игнорировать ошибки компиляции
только для данной задачи.

Смотри также
[`compile_error_penalty`](serve.cfg:problem:compile_error_penalty.md).
