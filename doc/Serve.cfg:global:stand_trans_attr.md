Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Глобальные
конфигурационные
параметры](serve.cfg:global "wikilink")/[`stand_trans_attr`](Serve.cfg:global:stand_trans_attr "wikilink")

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Global settings (serve.cfg)"*, блок *"Standings table attributes"*,
поле *"HTML attributes for transient cells"*.

Данная переменная вместе с переменной
[`stand_fail_attr`](serve.cfg:global:stand_fail_attr "wikilink")
позволяют определить атрибут ячейки таблицы текущих результатов, если
для данного пользователя и для данной задачи есть посылки в состоянии
"Check failed" и "Compiling..." или "Running..." соответственно. Атрибут
`stand_trans_attr` может использоваться для индикации того, что в данный
момент посылки тестируются, что может привести к изменению таблицы.
