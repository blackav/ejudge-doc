Навигация: [Система ejudge](Система_ejudge.md) /
[Использование](Использование.md) / [Использование из командной
строки](Использование_из_командной_строки.md) /
[ejudge-contests-cmd](ejudge-contests-cmd.md) /
[Команды](ejudge-contests-cmd:_COMMAND.md) /
[force-start-virtual](ejudge-contests-cmd:_force-start-virtual.md)

Команда force-start-virtual принудительно начинает виртуальный турнир
для указанного пользователя.

Использование:

`ejudge-contests-cmd CONTEST-ID force-start-virtual [OPTIONS] SESSION-FILE USER-ID`

Поддерживаются все [стандартные опции
команд](ejudge-contests-cmd:_COMMAND-OPTIONS.md). В частности,
если указана опция `--session`, то аргумент `SESSION-FILE` — это не
файл, в котором записан сессионный ключ, а сам сессионный ключ.

`USER-ID` — идентификатор пользователя.

Для выполнения команды требуются полномочия администратора турнира.
