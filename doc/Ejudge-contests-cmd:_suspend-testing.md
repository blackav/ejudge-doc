Навигация: [Система ejudge](Система_ejudge.md) /
[Использование](Использование.md) / [Использование из командной
строки](Использование_из_командной_строки.md) /
[ejudge-contests-cmd](ejudge-contests-cmd.md) /
[Команды](ejudge-contests-cmd:_COMMAND.md)

Команда suspend-testing приостанавливает тестирование поступающих
посылок. Поступающие посылки получат статус PENDING и могут быть
перетестированы позднее с помощью команды
[judge-suspended-runs](ejudge-contests-cmd:_judge-suspended-runs.md).
Для выполнения этой команды требуются полномочия администратора турнира.

См. также команды
[resume-testing](ejudge-contests-cmd:_resume-testing.md) и
[judge-suspended-runs](ejudge-contests-cmd:_judge-suspended-runs.md).

Использование:

`ejudge-contests-cmd CONTEST-ID suspend-testing [OPTIONS] SESSION-FILE`

Поддерживаются все [стандартные опции
команд](ejudge-contests-cmd:_COMMAND-OPTIONS.md). В частности,
если указана опция `--session`, то аргумент `SESSION-FILE` — это не
файл, в котором записан сессионный ключ, а сам сессионный ключ.
