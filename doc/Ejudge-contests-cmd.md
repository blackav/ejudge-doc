Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Использование
из командной
строки](Использование_из_командной_строки "wikilink")/[ejudge-contests-cmd](ejudge-contests-cmd "wikilink")

Программа ejudge-contests-cmd позволяет формировать запросы к серверу
турниров из командной строки.

Основные варианты использования:

`ejudge-contests-cmd --version`

печатает версию системы ejudge и время компиляции системы

`ejudge-contests-cmd --help`

печатает краткую подсказку об использовании программы

`ejudge-contests-cmd [GLOBAL-OPTIONS] CONTEST-ID COMMAND [COMMAND-OPTIONS] [COMMAND-ARGS]`

Здесь [GLOBAL-OPTIONS](ejudge-contests-cmd:_GLOBAL-OPTIONS "wikilink") —
это опции, позволяющие задать, например, путь к конфигурационному файлу
ejudge, CONTEST-ID — это номер турнира,
[COMMAND](ejudge-contests-cmd:_COMMAND "wikilink") — команда для
выполнения на сервере,
[COMMAND-OPTIONS](ejudge-contests-cmd:_COMMAND-OPTIONS "wikilink") —
дополнительные опции команды,
[COMMAND-ARGS](ejudge-contests-cmd:_COMMAND-ARGS "wikilink") — аргументы
команды.
