Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Глобальные
конфигурационные
параметры](serve.cfg:global "wikilink")/[`stand_show_ok_time`](Serve.cfg:global:stand_show_ok_time "wikilink")

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Global settings (serve.cfg)"*, блок *"Standings table attributes"*,
поле *"Show success time in standings"*.

Глобальная переменная действует только в режиме *KIROV*.

Если глобальная переменная `stand_show_ok_time` установлена в ненулевое
значение, в таблице текущих результатов печатается время успешной сдачи
задания (оно может быть как относительным от начала турнира, так и
астрономическим в зависимости от значения глобальной конфигурационной
переменной
[`show_astr_time`](serve.cfg:global:show_astr_time "wikilink")).
