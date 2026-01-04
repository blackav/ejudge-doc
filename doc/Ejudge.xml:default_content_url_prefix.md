Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[ejudge.xml](ejudge.xml "wikilink")/[`default_content_url_prefix`](ejudge.xml:default_content_url_prefix "wikilink")

Этот элемент позволяет задать префикс по умолчанию для [генерации
корректных URL аватаров](поддержка_аватаров "wikilink").

Например, если веб-сервер настроен таким образом, что аватары доступны
по URL вида <http://localhost/content/29211aapo72hvf0ltjvm2skq81.jpg>,
префикс аватаров может быть задан как <http://localhost/content/> или
лучше как /content/. Обратите внимание, что префикс должен заканчиваться
на знак /. Таким образом, значение элемента должно быть таким:

<default_content_url_prefix>`/content/`</default_content_url_prefix>

Поддерживается с версии [3.7.0](изменения_в_версии_3.7.0 "wikilink").
