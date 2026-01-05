Навигация: [Система ejudge](Система_ejudge.md) /
[Использование](Использование.md) / [Использование из командной
строки](Использование_из_командной_строки.md) /
[ejudge-contests-cmd](ejudge-contests-cmd.md) /
[Команды](ejudge-contests-cmd:_COMMAND.md)

Команда judge-suspended-runs отправляет на тестирование все посылки со
статусом PENDING. Для выполнения команды требуются полномочия
администратора турнира.

См. также команды
[suspend-testing](ejudge-contests-cmd:_suspend-testing.md) и
[resume-testing](ejudge-contests-cmd:_resume-testing.md).

Использование:

`ejudge-contests-cmd CONTEST-ID judge-suspended-runs [OPTIONS] SESSION-FILE`

Поддерживаются все [стандартные опции
команд](ejudge-contests-cmd:_COMMAND-OPTIONS.md). В частности,
если указана опция `--session`, то аргумент `SESSION-FILE` — это не
файл, в котором записан сессионный ключ, а сам сессионный ключ.
