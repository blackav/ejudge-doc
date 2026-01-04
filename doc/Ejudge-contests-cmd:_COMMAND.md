Навигация: [Система ejudge](Система_ejudge.md) /
[Использование](Использование.md) / [Использование из командной
строки](Использование_из_командной_строки.md) /
[ejudge-contests-cmd](ejudge-contests-cmd.md)/[COMMAND](Ejudge-contests-cmd:_COMMAND.md)

В настоящее время реализованы следующие команды:

|                                                                                    |                                                                                |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [login](ejudge-contests-cmd:_master-login.md)                              | создать сессионный ключ с правами администратора                               |
| [admin-login](ejudge-contests-cmd:_master-login.md)                        | создать сессионный ключ с правами администратора                               |
| [master-login](ejudge-contests-cmd:_master-login.md)                       | создать сессионный ключ с правами администратора                               |
| [judge-login](ejudge-contests-cmd:_judge-login.md)                         | создать сессионный ключ с правами судьи                                        |
| [chief-examiner-login](ejudge-contests-cmd:_chief-examiner-login.md)       | создать сессионный ключ с правами главного экзаменатора (не поддерживается)    |
| [coordinator-login](ejudge-contests-cmd:_coordinator-login.md)             | создать сессионный ключ с правами координатора (не поддерживается)             |
| [examiner-login](ejudge-contests-cmd:_examiner-login.md)                   | создать сессионный ключ с правами экзаменатора (не поддерживается)             |
| [observer-login](ejudge-contests-cmd:_observer-login.md)                   | создать сессионный ключ с правами наблюдателя (не поддерживается)              |
| [user-login](ejudge-contests-cmd:_user-login.md)                           | создать сессионный ключ с правами обычного (непривилегированного) пользователя |
| [logout](ejudge-contests-cmd:_logout.md)                                   | уничтожить сессионный ключ                                                     |
| [write-xml-runs](ejudge-contests-cmd:_write-xml-runs.md)                   | вывести список посылок во внутреннем XML-формате                               |
| [export-xml-runs](ejudge-contests-cmd:_export-xml-runs.md)                 | вывести список посылок во внешнем XML-формате                                  |
| [dump-all-runs](ejudge-contests-cmd:_dump-all-runs.md)                     | вывести список всех посылок в CSV-формате                                      |
| [dump-problems](ejudge-contests-cmd:_dump-problems.md)                     | вывести список задач в CSV-формате                                             |
| [soft-update-stand](ejudge-contests-cmd:_soft-update-stand.md)             | обновить таблицу текущих результатов, если не действует "заморозка"            |
| [suspend-testing](ejudge-contests-cmd:_suspend-testing.md)                 | приостановить тестирование поступающих посылок                                 |
| [resume-testing](ejudge-contests-cmd:_resume-testing.md)                   | возобновить тестирование поступающих посылок                                   |
| [judge-suspended-runs](ejudge-contests-cmd:_judge-suspended-runs.md)       | отправить на тестирование все посылки со статусом PENDING                      |
| [has-transient-runs](ejudge-contests-cmd:_has-transient-runs.md)           | проверить, если в данный момент тестируемые посылки                            |
| [run-status](ejudge-contests-cmd:_run-status.md)                           | вернуть статус посылки                                                         |
| [dump-source](ejudge-contests-cmd:_dump-source.md)                         | вывести исходный текст посылки                                                 |
| [dump-clar](ejudge-contests-cmd:_dump-clar.md)                             | вывести текст сообщения                                                        |
| [get-contest-name](ejudge-contests-cmd:_get-contest-name.md)               | вывести название турнира                                                       |
| [get-contest-type](ejudge-contests-cmd:_get-contest-type.md)               | вывести тип турнира                                                            |
| [submit-run](ejudge-contests-cmd:_submit-run.md)                           | послать решение на тестирование                                                |
| [import-xml-runs](ejudge-contests-cmd:_import-xml-runs.md)                 | загрузить посылки из заданного XML-файла                                       |
| [dump-filtered-runs](ejudge-contests-cmd:_dump-filtered-runs.md)           | вывести посылки в CSV-формате                                                  |
| [dump-report](ejudge-contests-cmd:_dump-report.md)                         | вывести протокол тестирования                                                  |
| [full-import-xml-runs](ejudge-contests-cmd:_full-import-xml-runs.md)       | загрузить посылки из заданного XML-файла                                       |
| [unload](ejudge-contests-cmd:_unload.md)                                   | выгрузить турнир из памяти сервера                                             |
| [start-contest](ejudge-contests-cmd:_start-contest.md)                     | начать турнир                                                                  |
| [stop-contest](ejudge-contests-cmd:_stop-contest.md)                       | закончить турнир                                                               |
| [continue-contest](ejudge-contests-cmd:_continue-contest.md)               | продолжить турнир                                                              |
| [suspend-contest](ejudge-contests-cmd:_suspend-contest.md)                 | приостановить турнир                                                           |
| [resume-contest](ejudge-contests-cmd:_resume-contest.md)                   | возобновить приостановленный турнир                                            |
| [suspend-printing](ejudge-contests-cmd:_suspend-printing.md)               | приостановить обработку запросов на печать посылок                             |
| [resume-printing](ejudge-contests-cmd:_resume-printing.md)                 | возобновить обработку запросов на печать посылок                               |
| [set-judging-mode](ejudge-contests-cmd:_set-judging-mode.md)               | переключить турнир в режим проверки решений                                    |
| [set-accepting-mode](ejudge-contests-cmd:_set-accepting-mode.md)           | переключить турнир в режим приема решений                                      |
| [set-testing-finished](ejudge-contests-cmd:_set-testing-finished.md)       | установить флаг окончания тестирования                                         |
| [clear-testing-finished](ejudge-contests-cmd:_clear-testing-finished.md)   | сбросить флаг окончания тестирования                                           |
| [rejudge-all](ejudge-contests-cmd:_rejudge-all.md)                         | перетестировать все посылки                                                    |
| [schedule](ejudge-contests-cmd:_schedule.md)                               | назначить время старта турнира                                                 |
| [force-start-virtual](ejudge-contests-cmd:_force-start-virtual.md)         | начать виртуальный турнир для указанного пользователя                          |
| [dump-languages](ejudge-contests-cmd:_dump-languages.md)                   | вывести список языков программирования турнира                                 |
| [get-contest-status](ejudge-contests-cmd:_get-contest-status.md)           | получить текущее состояние турнира                                             |
| [get-contest-sched](ejudge-contests-cmd:_get-contest-sched.md)             | получить запланированное время начала турнира                                  |
| [get-contest-duration](ejudge-contests-cmd:_get-contest-duration.md)       | получить продолжительность турнира                                             |
| [get-contest-description](ejudge-contests-cmd:_get-contest-description.md) | получить описание турнира                                                      |
| [unload-2](ejudge-contests-cmd:_unload-2.md)                               | выгрузить турнир из памяти сервера                                             |
