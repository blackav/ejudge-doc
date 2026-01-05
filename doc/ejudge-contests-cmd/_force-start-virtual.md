Навигация: [Система ejudge](../система_ejudge.md) /
[Использование](../использование.md) / [Использование из командной
строки](../использование_из_командной_строки.md) /
[ejudge-contests-cmd](../ejudge-contests-cmd.md) /
[Команды](_COMMAND.md) /
[force-start-virtual](_force-start-virtual.md)

Команда force-start-virtual принудительно начинает виртуальный турнир
для указанного пользователя.

Использование:

`ejudge-contests-cmd CONTEST-ID force-start-virtual [OPTIONS] SESSION-FILE USER-ID`

Поддерживаются все [стандартные опции
команд](_COMMAND-OPTIONS.md). В частности,
если указана опция `--session`, то аргумент `SESSION-FILE` — это не
файл, в котором записан сессионный ключ, а сам сессионный ключ.

`USER-ID` — идентификатор пользователя.

Для выполнения команды требуются полномочия администратора турнира.
