Навигация: [Система ejudge](../система_ejudge.md) /
[Использование](../использование.md) / [Использование из командной
строки](../использование_из_командной_строки.md) /
[ejudge-contests-cmd](../ejudge-contests-cmd.md) /
[Команды](_COMMAND.md)

Команда judge-suspended-runs отправляет на тестирование все посылки со
статусом PENDING. Для выполнения команды требуются полномочия
администратора турнира.

См. также команды
[suspend-testing](_suspend-testing.md) и
[resume-testing](_resume-testing.md).

Использование:

`ejudge-contests-cmd CONTEST-ID judge-suspended-runs [OPTIONS] SESSION-FILE`

Поддерживаются все [стандартные опции
команд](_COMMAND-OPTIONS.md). В частности,
если указана опция `--session`, то аргумент `SESSION-FILE` — это не
файл, в котором записан сессионный ключ, а сам сессионный ключ.
