Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[contest.xml](contest.xml "wikilink")/[`content_plugin`](contest.xml:content_plugin "wikilink")

Данный элемент позволяет задать имя плагина для [хранения аватаров в
файловой системе](поддержка_аватаров "wikilink"). Значение по умолчанию
для всех турниров может быть задано с помощью элемента
[`default_content_plugin`](ejudge.xml:default_content_plugin "wikilink")
в глобальном конфигурационном файле [ejudge.xml](ejudge.xml "wikilink").

Пример:

<content_plugin>`file`</content_plugin>

Поддерживается с версии [3.7.0](изменения_в_версии_3.7.0 "wikilink").
