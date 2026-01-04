Навигация: [Система ejudge](Система_ejudge "wikilink") /
[Использование](Использование "wikilink") / [Использование из командной
строки](Использование_из_командной_строки "wikilink") /
[ejudge-contests-cmd](ejudge-contests-cmd "wikilink") /
[Команды](ejudge-contests-cmd:_COMMAND "wikilink") /
[force-start-virtual](ejudge-contests-cmd:_force-start-virtual "wikilink")

Команда force-start-virtual принудительно начинает виртуальный турнир
для указанного пользователя.

Использование:

`ejudge-contests-cmd CONTEST-ID force-start-virtual [OPTIONS] SESSION-FILE USER-ID`

Поддерживаются все [стандартные опции
команд](ejudge-contests-cmd:_COMMAND-OPTIONS "wikilink"). В частности,
если указана опция `--session`, то аргумент `SESSION-FILE` — это не
файл, в котором записан сессионный ключ, а сам сессионный ключ.

`USER-ID` — идентификатор пользователя.

Для выполнения команды требуются полномочия администратора турнира.
