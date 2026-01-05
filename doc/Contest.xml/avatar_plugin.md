Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[contest.xml](contest.xml.md)/[`avatar_plugin`](contest.xml:avatar_plugin.md)

Данный элемент позволяет задать имя плагина для [хранения
аватаров](поддержка_аватаров.md). Значение по умолчанию для всех
турниров может быть задано с помощью элемента
[`default_avatar_plugin`](ejudge.xml:default_avatar_plugin.md) в
глобальном конфигурационном файле [ejudge.xml](ejudge.xml.md).

Пример:

<avatar_plugin>`mongo`</avatar_plugin>

Поддерживается с версии [3.7.0](изменения_в_версии_3.7.0.md).
