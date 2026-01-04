Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Инсталляция](Инсталляция "wikilink")/[Инсталляция
на ALT Linux](Инсталляция_на_ALT_Linux "wikilink")/[Запуск демонов
ejudge](Инсталляция_на_ALT_Linux:Запуск_демонов_ejudge "wikilink")

В дистрибутивах ALT Linux начиная с дистрибутивов, построенных на базе
"Седьмой платформы" - p7 используется systemd для запуска системных
служб.

Для запуска и остановки сервисов ejudge используются команды

`# systemctl start ejudge.service`  
`# systemctl stop ejudge.service`

Для автоматического запуска сервиса ejudge при старте системы
используйте команду

`# systemctl enable ejudge.service`

Помимо этого не забудьте об автозапуске сервисов httpd2 и mysqld:

`# systemctl enable httpd2.service`  
`# systemctl enable mysqld.service`

В дистрибутивах ALT Linux до "Шестой платформы" - p6 (включительно) для
запуска системных служб использовались System V init-скрипты.

В этих дистрибутивах для запуска и остановки сервисом ejudge необходимо
выполнить команду:

`# service ejudge start`  
`# service ejudge stop`

Для автоматического старта сервисов ejudge при запуске системы
используйте chkconfig:

`# chkconfig ejudge on`  
`# chkconfig httpd2 on`  
`# chkconfig mysqld on`
