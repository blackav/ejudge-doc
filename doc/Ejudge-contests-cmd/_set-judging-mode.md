Навигация: [Система ejudge](Система_ejudge.md) /
[Использование](Использование.md) / [Использование из командной
строки](Использование_из_командной_строки.md) /
[ejudge-contests-cmd](ejudge-contests-cmd.md) /
[Команды](ejudge-contests-cmd:_COMMAND.md)

Команда set-judging-mode переключает турнир в режим проверки решений.
Данная команда доступна только для турниров типа OLYMPIAD. Для
выполнения команды необходимы полномочия администратора турнира.

Использование:

`ejudge-contests-cmd CONTEST-ID set-judging-mode [OPTIONS] SESSION-FILE`

Поддерживаются все [стандартные опции
команд](ejudge-contests-cmd:_COMMAND-OPTIONS.md). В частности,
если указана опция `--session`, то аргумент `SESSION-FILE` — это не
файл, в котором записан сессионный ключ, а сам сессионный ключ.
