Навигация: [Система ejudge](Система_ejudge "wikilink") /
[Использование](Использование "wikilink") / [Использование из командной
строки](Использование_из_командной_строки "wikilink") /
[ejudge-contests-cmd](ejudge-contests-cmd "wikilink") /
[Команды](ejudge-contests-cmd:_COMMAND "wikilink")

Команда get-contest-type выводит на стандартный поток вывода тип
турнира.

Использование:

`ejudge-contests-cmd CONTEST-ID get-contest-type [OPTIONS] SESSION-FILE`

Поддерживаются все [стандартные опции
команд](ejudge-contests-cmd:_COMMAND-OPTIONS "wikilink"). В частности,
если указана опция `--session`, то аргумент `SESSION-FILE` — это не
файл, в котором записан сессионный ключ, а сам сессионный ключ.

В случае успешного выполнения команды на стандартный поток вывода будет
выведена одна из следующих строк:

|                  |                                  |
|------------------|----------------------------------|
| acm              | обычный турнир типа ACM          |
| acm-virtual      | виртуальный турнир типа ACM      |
| kirov            | турнир типа KIROV                |
| olympiad         | обычный турнир типа OLYMPIAD     |
| olympiad-virtual | виртуальный турнир типа OLYMPIAD |
| moscow           | турнир типа MOSCOW               |
