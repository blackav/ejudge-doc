Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Глобальные
конфигурационные
параметры](serve.cfg:global "wikilink")/[`tgzdir_sfx`](Serve.cfg:global:tgzdir_sfx "wikilink")

Данная глобальная конфигурационная переменная задает суффикс имен
эталонных рабочих каталогов для тестируемых программ. Суффикс
используется, если ни в абстрактной, ни в конкретной задаче не
определена конфигурационная переменная задачи
[`tgzdir_sfx`](Serve.cfg:problem:tgzdir_sfx "wikilink").

Если на глобальном уровне или уровне задачи определена конфигурационная
переменная [`tgzdir_pat`](Serve.cfg:global:tgzdir_pat "wikilink"), то
используется она, а конфигурационная переменная `tgzdir_sfx`
игнорируется.

Если ни одна из переменных
[`tgzdir_sfx`](Serve.cfg:global:tgzdir_sfx "wikilink"),
[`tgzdir_pat`](Serve.cfg:global:tgzdir_pat "wikilink"),
[`tgzdir_sfx`](Serve.cfg:problem:tgzdir_sfx "wikilink"),
[`tgzdir_pat`](Serve.cfg:problem:tgzdir_pat "wikilink") не определена,
используется суффикс по умолчанию `".dir"`.

Поддерживается с версии 2.3.20.
