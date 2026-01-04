Навигация: [Система ejudge](Система_ejudge "wikilink") /
[Использование](Использование "wikilink") / [Использование из командной
строки](Использование_из_командной_строки "wikilink") /
[ejudge-contests-cmd](ejudge-contests-cmd "wikilink") /
[Команды](ejudge-contests-cmd:_COMMAND "wikilink")

Команда rejudge-all запускает перетестирование всех посылок. Данную
команду может выполнять только администратор турнира.

Использование:

`ejudge-contests-cmd CONTEST-ID rejudge-all [OPTIONS] SESSION-FILE`

Поддерживаются все [стандартные опции
команд](ejudge-contests-cmd:_COMMAND-OPTIONS "wikilink"). В частности,
если указана опция `--session`, то аргумент `SESSION-FILE` — это не
файл, в котором записан сессионный ключ, а сам сессионный ключ.
