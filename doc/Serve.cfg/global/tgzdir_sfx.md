Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Глобальные
конфигурационные
параметры](serve.cfg:global.md)/[`tgzdir_sfx`](Serve.cfg:global:tgzdir_sfx.md)

Данная глобальная конфигурационная переменная задает суффикс имен
эталонных рабочих каталогов для тестируемых программ. Суффикс
используется, если ни в абстрактной, ни в конкретной задаче не
определена конфигурационная переменная задачи
[`tgzdir_sfx`](Serve.cfg:problem:tgzdir_sfx.md).

Если на глобальном уровне или уровне задачи определена конфигурационная
переменная [`tgzdir_pat`](Serve.cfg:global:tgzdir_pat.md), то
используется она, а конфигурационная переменная `tgzdir_sfx`
игнорируется.

Если ни одна из переменных
[`tgzdir_sfx`](Serve.cfg:global:tgzdir_sfx.md),
[`tgzdir_pat`](Serve.cfg:global:tgzdir_pat.md),
[`tgzdir_sfx`](Serve.cfg:problem:tgzdir_sfx.md),
[`tgzdir_pat`](Serve.cfg:problem:tgzdir_pat.md) не определена,
используется суффикс по умолчанию `".dir"`.

Поддерживается с версии 2.3.20.
