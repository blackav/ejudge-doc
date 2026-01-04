Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Конфигурационные
параметры
задач](serve.cfg:problem.md)/[`time_limit_millis`](serve.cfg:problem:time_limit_millis.md)

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Abstract problems"*, поле *"Processor
time limit (ms, ovverides prev. limit)"*, либо страница *"Editing
contest"*, вкладка *"Problems (serve.cfg)"*, блок *"Concrete problems"*,
поле *"Processor time limit (ms, ovverides prev. limit)"*.

Данная переменная позволяет устанавливать ограничение времени с
точностью до миллисекунды.

Если установлена данная переменная, значение переменной
[`time_limit`](serve.cfg:problem:time_limit.md) игнорируется.
Поддержка миллисекундных ограничений времени работает только, если
используется последняя версия библиотеки `reuse` (4.2.0). Если ядро
`Linux` не поддерживает миллисекундные ограничения времени, `reuse`
будет эмулировать их с помощью секундных ограничений времени.
