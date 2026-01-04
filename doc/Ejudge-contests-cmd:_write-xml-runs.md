Навигация: [Система ejudge](Система_ejudge "wikilink") /
[Использование](Использование "wikilink") / [Использование из командной
строки](Использование_из_командной_строки "wikilink") /
[ejudge-contests-cmd](ejudge-contests-cmd "wikilink") /
[Команды](ejudge-contests-cmd:_COMMAND "wikilink")

Команда write-xml-runs выводит на стандартный поток вывода базу посылок
во внутреннем XML-формате. Для выполнения этой команды необходимы
полномочия администратора турнира.

Использование:

`ejudge-contests-cmd CONTEST-ID write-xml-runs [OPTIONS] SESSION-FILE`

Поддерживаются все [стандартные опции
команд](ejudge-contests-cmd:_COMMAND-OPTIONS "wikilink"). В частности,
если указана опция `--session`, то аргумент `SESSION-FILE` — это не
файл, в котором записан сессионный ключ, а сам сессионный ключ.

См. также команду
[export-xml-runs](ejudge-contests-cmd:_export-xml-runs "wikilink").
