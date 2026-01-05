Навигация: [Главная страница](../../main_Page.md)/[Система
ejudge](../../система_ejudge.md)/[Использование](../../использование.md)/[Конфигурационные
файлы](../../конфигурационные_файлы.md)/[serve.cfg](../../serve.cfg.md)/[Конфигурационные
параметры
задач](../problem.md)/[ignore_compile_errors](ignore_compile_errors.md)

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Abstract problems"*, поле *"Ignore
compilation errors"*, либо страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Concrete problems"*, поле *"Ignore
compilation errors"*.

Эта переменная позволяет переопределить действие глобальной
конфигурационной переменной
[`ignore_compile_errors`](../global/ignore_compile_errors.md)
для одной задачи. Например, если глобальная переменная установлена (то
есть ошибки компиляции игнорируются при подсчёте результатов), строка

`ignore_compile_errors = 0`

раздела определения задачи позволит не игнорировать ошибки компиляции
только для данной задачи.

Смотри также
[`compile_error_penalty`](compile_error_penalty.md).
