Навигация: [Система ejudge](Система_ejudge.md) /
[Использование](Использование.md) / [Использование из командной
строки](Использование_из_командной_строки.md) /
[ejudge-contests-cmd](ejudge-contests-cmd.md) /
[Команды](ejudge-contests-cmd:_COMMAND.md)

Команда dump-clar выводит на стандартный поток вывода указанное
сообщение.

Использование:

`ejudge-contests-cmd CONTEST-ID dump-clar [OPTIONS] SESSION-FILE CLAR-ID`

Поддерживаются все [стандартные опции
команд](ejudge-contests-cmd:_COMMAND-OPTIONS.md). В частности,
если указана опция `--session`, то аргумент `SESSION-FILE` — это не
файл, в котором записан сессионный ключ, а сам сессионный ключ.

`CLAR-ID` — идентификатор (номер) сообщения.
