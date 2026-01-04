Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[lang_time_adj_millis](serve.cfg:problem:lang_time_adj_millis "wikilink")

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Concrete problems"*, поле
*"Language-based time-limit adjustment (ms)"*.

Данная переменная аналогична переменной
[`lang_time_adj`](serve.cfg:problem:lang_time_adj "wikilink"), то есть
позволяет задавать поправку к ограничению времени на тест в зависимости
от языка программирования, но значение поправки выражается в
миллисекундах. Переменная `lang_time_adj_millis` имеет приоритет над
переменной
[`lang_time_adj`](serve.cfg:problem:lang_time_adj "wikilink"), то есть
если задано значение первой переменной, то вторая не используется.
