Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[ejudge.xml](ejudge.xml.md)/[`config`](ejudge.xml:config.md)/[`enable_telegram_registration`](ejudge.xml:config:enable_telegram_registration.md)

Атрибут `enable_telegram_registration` корневого элемента
[`config`](ejudge.xml:config.md) позволяет разрешить регистрацию
новых пользователей ejudge и регистрации на турнры с помощью
[Telegram-бота](Telegram_bot:_регистрация_на_турнир.md).

Для каждого турнира, для которого должна быть разрешена
Telegram-регистрация, должен быть установлен атрибут
[`enable_telegram_registration`](contest.xml:enable_telegram_registration.md).

Пример:

<config enable_telegram_registration="yes">

Поддерживается начиная с версии
[3.12.0](изменения_в_версии_3.12.0.md).
