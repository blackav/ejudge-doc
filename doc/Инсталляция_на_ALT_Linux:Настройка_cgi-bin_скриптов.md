Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Инсталляция](Инсталляция "wikilink")/[Инсталляция
на ALT Linux](Инсталляция_на_ALT_Linux "wikilink")/[Настройка cgi-bin
скриптов](Инсталляция_на_ALT_Linux:Настройка_cgi-bin_скриптов "wikilink")

Для работы ejudge необходим web-сервер apache2. Работа ejudge с прочими
web-серверами не тестировалась.

Apache должен быть настроен на исполнение cgi-bin программ. Выполните
следующие команды от пользователя root для разрешения исполнения cgi-bin
программ:

`# a2enmod cgi`  
`# service httpd2 restart`
