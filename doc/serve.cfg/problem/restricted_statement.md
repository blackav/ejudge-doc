Навигация: [Главная страница](../../main_Page.md)/[Система
ejudge](../../система_ejudge.md)/[Использование](../../использование.md)/[Конфигурационные
файлы](../../конфигурационные_файлы.md)/[serve.cfg](../../serve.cfg.md)/[Конфигурационные
параметры
задач](../problem.md)/[restricted_statement](restricted_statement.md)

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Abstract problems"*, поле *"Restricted
problem statement"*, либо страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Concrete problems"*, поле *"Restricted
problem statement"*.

Если значение этой переменной не равно 0, условие данной задачи
перестанет отображаться после конца турнира или после момента закрытия
сдачи этой задачи (установленного переменной
[`deadline`](deadline.md)). По умолчанию
условия задач <b>не отображаются</b> после окончания турнира или
закрытия сдачи задачи.

<b>Эта конфигурационная переменная никогда не работала правильно.</b>

Начиная с версии [3.1.0](../../изменения_в_версии_3.1.0.md) значение
конфигурационной переменной
[restricted_statement](restricted_statement.md)
игнорируется. Используйте конфигурационную переменную
[unrestricted_statement](unrestricted_statement.md).
