Навигация: [Система ejudge](../система_ejudge.md) /
[Использование](../использование.md) / [Использование из командной
строки](../использование_из_командной_строки.md) /
[ejudge-contests-cmd](../ejudge-contests-cmd.md)/[COMMAND](_COMMAND.md)

В настоящее время реализованы следующие команды:

|                                                                                    |                                                                                |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [login](_master-login.md)                              | создать сессионный ключ с правами администратора                               |
| [admin-login](_master-login.md)                        | создать сессионный ключ с правами администратора                               |
| [master-login](_master-login.md)                       | создать сессионный ключ с правами администратора                               |
| [judge-login](_judge-login.md)                         | создать сессионный ключ с правами судьи                                        |
| [chief-examiner-login](ejudge-contests-cmd:_chief-examiner-login.md)       | создать сессионный ключ с правами главного экзаменатора (не поддерживается)    |
| [coordinator-login](ejudge-contests-cmd:_coordinator-login.md)             | создать сессионный ключ с правами координатора (не поддерживается)             |
| [examiner-login](ejudge-contests-cmd:_examiner-login.md)                   | создать сессионный ключ с правами экзаменатора (не поддерживается)             |
| [observer-login](ejudge-contests-cmd:_observer-login.md)                   | создать сессионный ключ с правами наблюдателя (не поддерживается)              |
| [user-login](_user-login.md)                           | создать сессионный ключ с правами обычного (непривилегированного) пользователя |
| [logout](_logout.md)                                   | уничтожить сессионный ключ                                                     |
| [write-xml-runs](_write-xml-runs.md)                   | вывести список посылок во внутреннем XML-формате                               |
| [export-xml-runs](_export-xml-runs.md)                 | вывести список посылок во внешнем XML-формате                                  |
| [dump-all-runs](_dump-all-runs.md)                     | вывести список всех посылок в CSV-формате                                      |
| [dump-problems](_dump-problems.md)                     | вывести список задач в CSV-формате                                             |
| [soft-update-stand](_soft-update-stand.md)             | обновить таблицу текущих результатов, если не действует "заморозка"            |
| [suspend-testing](_suspend-testing.md)                 | приостановить тестирование поступающих посылок                                 |
| [resume-testing](_resume-testing.md)                   | возобновить тестирование поступающих посылок                                   |
| [judge-suspended-runs](_judge-suspended-runs.md)       | отправить на тестирование все посылки со статусом PENDING                      |
| [has-transient-runs](_has-transient-runs.md)           | проверить, если в данный момент тестируемые посылки                            |
| [run-status](_run-status.md)                           | вернуть статус посылки                                                         |
| [dump-source](_dump-source.md)                         | вывести исходный текст посылки                                                 |
| [dump-clar](_dump-clar.md)                             | вывести текст сообщения                                                        |
| [get-contest-name](_get-contest-name.md)               | вывести название турнира                                                       |
| [get-contest-type](_get-contest-type.md)               | вывести тип турнира                                                            |
| [submit-run](_submit-run.md)                           | послать решение на тестирование                                                |
| [import-xml-runs](_import-xml-runs.md)                 | загрузить посылки из заданного XML-файла                                       |
| [dump-filtered-runs](_dump-filtered-runs.md)           | вывести посылки в CSV-формате                                                  |
| [dump-report](_dump-report.md)                         | вывести протокол тестирования                                                  |
| [full-import-xml-runs](_full-import-xml-runs.md)       | загрузить посылки из заданного XML-файла                                       |
| [unload](_unload.md)                                   | выгрузить турнир из памяти сервера                                             |
| [start-contest](_start-contest.md)                     | начать турнир                                                                  |
| [stop-contest](_stop-contest.md)                       | закончить турнир                                                               |
| [continue-contest](_continue-contest.md)               | продолжить турнир                                                              |
| [suspend-contest](_suspend-contest.md)                 | приостановить турнир                                                           |
| [resume-contest](_resume-contest.md)                   | возобновить приостановленный турнир                                            |
| [suspend-printing](_suspend-printing.md)               | приостановить обработку запросов на печать посылок                             |
| [resume-printing](_resume-printing.md)                 | возобновить обработку запросов на печать посылок                               |
| [set-judging-mode](_set-judging-mode.md)               | переключить турнир в режим проверки решений                                    |
| [set-accepting-mode](_set-accepting-mode.md)           | переключить турнир в режим приема решений                                      |
| [set-testing-finished](_set-testing-finished.md)       | установить флаг окончания тестирования                                         |
| [clear-testing-finished](_clear-testing-finished.md)   | сбросить флаг окончания тестирования                                           |
| [rejudge-all](_rejudge-all.md)                         | перетестировать все посылки                                                    |
| [schedule](_schedule.md)                               | назначить время старта турнира                                                 |
| [force-start-virtual](_force-start-virtual.md)         | начать виртуальный турнир для указанного пользователя                          |
| [dump-languages](ejudge-contests-cmd:_dump-languages.md)                   | вывести список языков программирования турнира                                 |
| [get-contest-status](ejudge-contests-cmd:_get-contest-status.md)           | получить текущее состояние турнира                                             |
| [get-contest-sched](ejudge-contests-cmd:_get-contest-sched.md)             | получить запланированное время начала турнира                                  |
| [get-contest-duration](ejudge-contests-cmd:_get-contest-duration.md)       | получить продолжительность турнира                                             |
| [get-contest-description](ejudge-contests-cmd:_get-contest-description.md) | получить описание турнира                                                      |
| [unload-2](_unload-2.md)                               | выгрузить турнир из памяти сервера                                             |
