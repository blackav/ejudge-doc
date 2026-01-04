Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[ejudge.xml](ejudge.xml "wikilink")/[`config`](ejudge.xml:config "wikilink")/[`enable_telegram_registration`](ejudge.xml:config:enable_telegram_registration "wikilink")

Атрибут `enable_telegram_registration` корневого элемента
[`config`](ejudge.xml:config "wikilink") позволяет разрешить регистрацию
новых пользователей ejudge и регистрации на турнры с помощью
[Telegram-бота](Telegram_bot:_регистрация_на_турнир "wikilink").

Для каждого турнира, для которого должна быть разрешена
Telegram-регистрация, должен быть установлен атрибут
[`enable_telegram_registration`](contest.xml:enable_telegram_registration "wikilink").

Пример:

<config enable_telegram_registration="yes">

Поддерживается начиная с версии
[3.12.0](изменения_в_версии_3.12.0 "wikilink").
