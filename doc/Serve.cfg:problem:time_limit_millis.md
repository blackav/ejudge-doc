Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[`time_limit_millis`](serve.cfg:problem:time_limit_millis "wikilink")

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Abstract problems"*, поле *"Processor
time limit (ms, ovverides prev. limit)"*, либо страница *"Editing
contest"*, вкладка *"Problems (serve.cfg)"*, блок *"Concrete problems"*,
поле *"Processor time limit (ms, ovverides prev. limit)"*.

Данная переменная позволяет устанавливать ограничение времени с
точностью до миллисекунды.

Если установлена данная переменная, значение переменной
[`time_limit`](serve.cfg:problem:time_limit "wikilink") игнорируется.
Поддержка миллисекундных ограничений времени работает только, если
используется последняя версия библиотеки `reuse` (4.2.0). Если ядро
`Linux` не поддерживает миллисекундные ограничения времени, `reuse`
будет эмулировать их с помощью секундных ограничений времени.
