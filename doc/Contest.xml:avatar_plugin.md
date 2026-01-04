Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[contest.xml](contest.xml "wikilink")/[`avatar_plugin`](contest.xml:avatar_plugin "wikilink")

Данный элемент позволяет задать имя плагина для [хранения
аватаров](поддержка_аватаров "wikilink"). Значение по умолчанию для всех
турниров может быть задано с помощью элемента
[`default_avatar_plugin`](ejudge.xml:default_avatar_plugin "wikilink") в
глобальном конфигурационном файле [ejudge.xml](ejudge.xml "wikilink").

Пример:

<avatar_plugin>`mongo`</avatar_plugin>

Поддерживается с версии [3.7.0](изменения_в_версии_3.7.0 "wikilink").
