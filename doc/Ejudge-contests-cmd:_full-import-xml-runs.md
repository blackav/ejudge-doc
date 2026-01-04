Навигация: [Система ejudge](Система_ejudge "wikilink") /
[Использование](Использование "wikilink") / [Использование из командной
строки](Использование_из_командной_строки "wikilink") /
[ejudge-contests-cmd](ejudge-contests-cmd "wikilink") /
[Команды](ejudge-contests-cmd:_COMMAND "wikilink")

Команда full-import-xml-runs выполняет слияние базы посылок в
XML-формате из указанного файла и базы посылок турнира. При слиянии
учитываются и не дублируются записи об одной и той же посылке,
находящиеся и в базе посылок турнира, и в XML-файле. Таким образом,
операция слияния баз посылок, где в качестве XML-файла передаётся база
посылок текущего турнира, например, на накоторый момент времени в
прошлом, не приведет к изменению базы посылок.

Для выполнения этой команды необходимы полномочия администратора
турнира.

В отличие от команды
[import-xml-runs](ejudge-contests-cmd:_import-xml-runs "wikilink")
данная команда выполняет слияние баз посылок даже если в базе посылок
турнира есть посылки в состоянии компиляции или тестирования. Для этого
слияние выполняется в несколько шагов:

- приостанавливается тестирование поступающих посылок;
- ожидается окончание тестирования всех посылок в турнире;
- выполняется слияние баз посылок;
- возобновляется тестирование поступающих посылок;
- запускается тестирование всех принятых, но не протестированных
  посылок.

Использование:

`ejudge-contests-cmd CONTEST-ID full-import-xml-runs [OPTIONS] SESSION-FILE XML-FILE`

Поддерживаются все [стандартные опции
команд](ejudge-contests-cmd:_COMMAND-OPTIONS "wikilink"). В частности,
если указана опция `--session`, то аргумент `SESSION-FILE` — это не
файл, в котором записан сессионный ключ, а сам сессионный ключ.

Параметр `XML-FILE` — это имя файла с базой посылок в XML-формате. Если
значение параметра равно `STDIN` база посылок считывается со
стандартного потока ввода.

См. также команды:
[write-xml-runs](ejudge-contests-cmd:_write-xml-runs "wikilink"),
[export-xml-runs](ejudge-contests-cmd:_export-xml-runs "wikilink"),
[has-transient-runs](ejudge-contests-cmd:_has-transient-runs "wikilink"),
[import-xml-runs](ejudge-contests-cmd:_import-xml-runs "wikilink"),
[suspend-testing](ejudge-contests-cmd:_suspend-testing "wikilink"),
[resume-testing](ejudge-contests-cmd:_resume-testing "wikilink").
