Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[ejudge.xml](ejudge.xml "wikilink")/[`default_variant_plugin`](ejudge.xml:default_variant_plugin "wikilink")

Данный элемент позволяет задать плагин, который будет использоваться по
умолчанию для хранения информации о вариантах задач, назначенных
пользователям в вариантных задачах.

Поддерживается два плагина:

- `file` — хранение информации в текстовом файле `variant.map`.
- `mysql` — хранение информации в базе MySQL/MariaDB.

Для конкретного турнира плагин может быть назначен с помощью глобального
конфигурационного параметра
[`variant_plugin`](Serve.cfg:global:variant_plugin "wikilink").

<b>Пример.</b>

<default_variant_plugin>`mysql`</default_variant_plugin>

Поддерживается с версии [3.10.0](изменения_в_версии_3.10.0 "wikilink").
