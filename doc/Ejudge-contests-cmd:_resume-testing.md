Навигация: [Система ejudge](Система_ejudge "wikilink") /
[Использование](Использование "wikilink") / [Использование из командной
строки](Использование_из_командной_строки "wikilink") /
[ejudge-contests-cmd](ejudge-contests-cmd "wikilink") /
[Команды](ejudge-contests-cmd:_COMMAND "wikilink")

Команда resume-testing возобновляет тестирование поступающих посылок.
Для выполнения команды необходимы полномочия администратора турнира.

См. также команды
[suspend-testing](ejudge-contests-cmd:_suspend-testing "wikilink") и
[judge-suspended-runs](ejudge-contests-cmd:_judge-suspended-runs "wikilink").

Использование:

`ejudge-contests-cmd CONTEST-ID resume-testing [OPTIONS] SESSION-FILE`

Поддерживаются все [стандартные опции
команд](ejudge-contests-cmd:_COMMAND-OPTIONS "wikilink"). В частности,
если указана опция `--session`, то аргумент `SESSION-FILE` — это не
файл, в котором записан сессионный ключ, а сам сессионный ключ.
