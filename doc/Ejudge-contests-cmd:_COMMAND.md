Навигация: [Система ejudge](Система_ejudge "wikilink") /
[Использование](Использование "wikilink") / [Использование из командной
строки](Использование_из_командной_строки "wikilink") /
[ejudge-contests-cmd](ejudge-contests-cmd "wikilink")/[COMMAND](Ejudge-contests-cmd:_COMMAND "wikilink")

В настоящее время реализованы следующие команды:

|                                                                                    |                                                                                |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [login](ejudge-contests-cmd:_master-login "wikilink")                              | создать сессионный ключ с правами администратора                               |
| [admin-login](ejudge-contests-cmd:_master-login "wikilink")                        | создать сессионный ключ с правами администратора                               |
| [master-login](ejudge-contests-cmd:_master-login "wikilink")                       | создать сессионный ключ с правами администратора                               |
| [judge-login](ejudge-contests-cmd:_judge-login "wikilink")                         | создать сессионный ключ с правами судьи                                        |
| [chief-examiner-login](ejudge-contests-cmd:_chief-examiner-login "wikilink")       | создать сессионный ключ с правами главного экзаменатора (не поддерживается)    |
| [coordinator-login](ejudge-contests-cmd:_coordinator-login "wikilink")             | создать сессионный ключ с правами координатора (не поддерживается)             |
| [examiner-login](ejudge-contests-cmd:_examiner-login "wikilink")                   | создать сессионный ключ с правами экзаменатора (не поддерживается)             |
| [observer-login](ejudge-contests-cmd:_observer-login "wikilink")                   | создать сессионный ключ с правами наблюдателя (не поддерживается)              |
| [user-login](ejudge-contests-cmd:_user-login "wikilink")                           | создать сессионный ключ с правами обычного (непривилегированного) пользователя |
| [logout](ejudge-contests-cmd:_logout "wikilink")                                   | уничтожить сессионный ключ                                                     |
| [write-xml-runs](ejudge-contests-cmd:_write-xml-runs "wikilink")                   | вывести список посылок во внутреннем XML-формате                               |
| [export-xml-runs](ejudge-contests-cmd:_export-xml-runs "wikilink")                 | вывести список посылок во внешнем XML-формате                                  |
| [dump-all-runs](ejudge-contests-cmd:_dump-all-runs "wikilink")                     | вывести список всех посылок в CSV-формате                                      |
| [dump-problems](ejudge-contests-cmd:_dump-problems "wikilink")                     | вывести список задач в CSV-формате                                             |
| [soft-update-stand](ejudge-contests-cmd:_soft-update-stand "wikilink")             | обновить таблицу текущих результатов, если не действует "заморозка"            |
| [suspend-testing](ejudge-contests-cmd:_suspend-testing "wikilink")                 | приостановить тестирование поступающих посылок                                 |
| [resume-testing](ejudge-contests-cmd:_resume-testing "wikilink")                   | возобновить тестирование поступающих посылок                                   |
| [judge-suspended-runs](ejudge-contests-cmd:_judge-suspended-runs "wikilink")       | отправить на тестирование все посылки со статусом PENDING                      |
| [has-transient-runs](ejudge-contests-cmd:_has-transient-runs "wikilink")           | проверить, если в данный момент тестируемые посылки                            |
| [run-status](ejudge-contests-cmd:_run-status "wikilink")                           | вернуть статус посылки                                                         |
| [dump-source](ejudge-contests-cmd:_dump-source "wikilink")                         | вывести исходный текст посылки                                                 |
| [dump-clar](ejudge-contests-cmd:_dump-clar "wikilink")                             | вывести текст сообщения                                                        |
| [get-contest-name](ejudge-contests-cmd:_get-contest-name "wikilink")               | вывести название турнира                                                       |
| [get-contest-type](ejudge-contests-cmd:_get-contest-type "wikilink")               | вывести тип турнира                                                            |
| [submit-run](ejudge-contests-cmd:_submit-run "wikilink")                           | послать решение на тестирование                                                |
| [import-xml-runs](ejudge-contests-cmd:_import-xml-runs "wikilink")                 | загрузить посылки из заданного XML-файла                                       |
| [dump-filtered-runs](ejudge-contests-cmd:_dump-filtered-runs "wikilink")           | вывести посылки в CSV-формате                                                  |
| [dump-report](ejudge-contests-cmd:_dump-report "wikilink")                         | вывести протокол тестирования                                                  |
| [full-import-xml-runs](ejudge-contests-cmd:_full-import-xml-runs "wikilink")       | загрузить посылки из заданного XML-файла                                       |
| [unload](ejudge-contests-cmd:_unload "wikilink")                                   | выгрузить турнир из памяти сервера                                             |
| [start-contest](ejudge-contests-cmd:_start-contest "wikilink")                     | начать турнир                                                                  |
| [stop-contest](ejudge-contests-cmd:_stop-contest "wikilink")                       | закончить турнир                                                               |
| [continue-contest](ejudge-contests-cmd:_continue-contest "wikilink")               | продолжить турнир                                                              |
| [suspend-contest](ejudge-contests-cmd:_suspend-contest "wikilink")                 | приостановить турнир                                                           |
| [resume-contest](ejudge-contests-cmd:_resume-contest "wikilink")                   | возобновить приостановленный турнир                                            |
| [suspend-printing](ejudge-contests-cmd:_suspend-printing "wikilink")               | приостановить обработку запросов на печать посылок                             |
| [resume-printing](ejudge-contests-cmd:_resume-printing "wikilink")                 | возобновить обработку запросов на печать посылок                               |
| [set-judging-mode](ejudge-contests-cmd:_set-judging-mode "wikilink")               | переключить турнир в режим проверки решений                                    |
| [set-accepting-mode](ejudge-contests-cmd:_set-accepting-mode "wikilink")           | переключить турнир в режим приема решений                                      |
| [set-testing-finished](ejudge-contests-cmd:_set-testing-finished "wikilink")       | установить флаг окончания тестирования                                         |
| [clear-testing-finished](ejudge-contests-cmd:_clear-testing-finished "wikilink")   | сбросить флаг окончания тестирования                                           |
| [rejudge-all](ejudge-contests-cmd:_rejudge-all "wikilink")                         | перетестировать все посылки                                                    |
| [schedule](ejudge-contests-cmd:_schedule "wikilink")                               | назначить время старта турнира                                                 |
| [force-start-virtual](ejudge-contests-cmd:_force-start-virtual "wikilink")         | начать виртуальный турнир для указанного пользователя                          |
| [dump-languages](ejudge-contests-cmd:_dump-languages "wikilink")                   | вывести список языков программирования турнира                                 |
| [get-contest-status](ejudge-contests-cmd:_get-contest-status "wikilink")           | получить текущее состояние турнира                                             |
| [get-contest-sched](ejudge-contests-cmd:_get-contest-sched "wikilink")             | получить запланированное время начала турнира                                  |
| [get-contest-duration](ejudge-contests-cmd:_get-contest-duration "wikilink")       | получить продолжительность турнира                                             |
| [get-contest-description](ejudge-contests-cmd:_get-contest-description "wikilink") | получить описание турнира                                                      |
| [unload-2](ejudge-contests-cmd:_unload-2 "wikilink")                               | выгрузить турнир из памяти сервера                                             |
