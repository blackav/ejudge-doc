Навигация: [Главная страница](../../main_Page.md)/[Система
ejudge](../../система_ejudge.md)/[Использование](../../использование.md)/[Конфигурационные
файлы](../../конфигурационные_файлы.md)/[ejudge.xml](../../ejudge.xml.md)/[`config`](../config.md)/[`enable_telegram_registration`](enable_telegram_registration.md)

Атрибут `enable_telegram_registration` корневого элемента
[`config`](../config.md) позволяет разрешить регистрацию
новых пользователей ejudge и регистрации на турнры с помощью
[Telegram-бота](../../telegram_bot/_регистрация_на_турнир.md).

Для каждого турнира, для которого должна быть разрешена
Telegram-регистрация, должен быть установлен атрибут
[`enable_telegram_registration`](../../contest.xml/enable_telegram_registration.md).

Пример:

<config enable_telegram_registration="yes">

Поддерживается начиная с версии
[3.12.0](../../изменения_в_версии_3.12.0.md).
