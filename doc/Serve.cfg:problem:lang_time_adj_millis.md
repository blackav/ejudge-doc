Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Конфигурационные
параметры
задач](serve.cfg:problem.md)/[lang_time_adj_millis](serve.cfg:problem:lang_time_adj_millis.md)

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Concrete problems"*, поле
*"Language-based time-limit adjustment (ms)"*.

Данная переменная аналогична переменной
[`lang_time_adj`](serve.cfg:problem:lang_time_adj.md), то есть
позволяет задавать поправку к ограничению времени на тест в зависимости
от языка программирования, но значение поправки выражается в
миллисекундах. Переменная `lang_time_adj_millis` имеет приоритет над
переменной
[`lang_time_adj`](serve.cfg:problem:lang_time_adj.md), то есть
если задано значение первой переменной, то вторая не используется.
