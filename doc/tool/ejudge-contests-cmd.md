Навигация: [Главная страница](main_Page.md)/[Система
ejudge](система_ejudge.md)/[Использование](использование.md)/[Использование
из командной
строки](использование_из_командной_строки.md)/[ejudge-contests-cmd](ejudge-contests-cmd.md)

Программа ejudge-contests-cmd позволяет формировать запросы к серверу
турниров из командной строки.

Основные варианты использования:

`ejudge-contests-cmd --version`

печатает версию системы ejudge и время компиляции системы

`ejudge-contests-cmd --help`

печатает краткую подсказку об использовании программы

`ejudge-contests-cmd [GLOBAL-OPTIONS] CONTEST-ID COMMAND [COMMAND-OPTIONS] [COMMAND-ARGS]`

Здесь [GLOBAL-OPTIONS](ejudge-contests-cmd/_GLOBAL-OPTIONS.md) —
это опции, позволяющие задать, например, путь к конфигурационному файлу
ejudge, CONTEST-ID — это номер турнира,
[COMMAND](ejudge-contests-cmd/_COMMAND.md) — команда для
выполнения на сервере,
[COMMAND-OPTIONS](ejudge-contests-cmd/_COMMAND-OPTIONS.md) —
дополнительные опции команды,
[COMMAND-ARGS](ejudge-contests-cmd/_COMMAND-ARGS.md) — аргументы
команды.
