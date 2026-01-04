Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Глобальные
конфигурационные
параметры](serve.cfg:global "wikilink")/[`tgzdir_pat`](Serve.cfg:global:tgzdir_pat "wikilink")

Данная глобальная конфигурационная переменная задает шаблон имен
эталонных рабочих каталогов для тестируемых программ. Шаблон
используется, если ни в абстрактной, ни в конкретной задаче не
определена конфигурационная переменная задачи
[`tgzdir_pat`](Serve.cfg:problem:tgzdir_pat "wikilink").

Если ни глобальная конфигурационная переменная
[`tgzdir_pat`](Serve.cfg:global:tgzdir_pat "wikilink"), ни
конфигурационные переменные задачи
[`tgzdir_pat`](Serve.cfg:problem:tgzdir_pat "wikilink") не определены,
то используются конфигурационные переменные, задающие суффикс имен
эталонных рабочих каталогов
[`tgzdir_sfx`](Serve.cfg:problem:tgzdir_sfx "wikilink").

Поддерживается с версии 2.3.20.
