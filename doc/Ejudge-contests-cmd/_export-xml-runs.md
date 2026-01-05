Навигация: [Система ejudge](Система_ejudge.md) /
[Использование](Использование.md) / [Использование из командной
строки](Использование_из_командной_строки.md) /
[ejudge-contests-cmd](ejudge-contests-cmd.md) /
[Команды](ejudge-contests-cmd:_COMMAND.md)

Команда export-xml-runs выводит на стандартный поток вывода базу посылок
во внешнем XML-формате. Для выполнения этой команды необходимы
полномочия администратора турнира.

Использование:

`ejudge-contests-cmd CONTEST-ID export-xml-runs [OPTIONS] SESSION-FILE`

Поддерживаются все [стандартные опции
команд](ejudge-contests-cmd:_COMMAND-OPTIONS.md). В частности,
если указана опция `--session`, то аргумент `SESSION-FILE` — это не
файл, в котором записан сессионный ключ, а сам сессионный ключ.

См. также команду
[write-xml-runs](ejudge-contests-cmd:_write-xml-runs.md).
