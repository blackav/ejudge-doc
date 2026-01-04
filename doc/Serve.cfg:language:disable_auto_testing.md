Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
языков](serve.cfg:language "wikilink")/[disable_auto_testing](Serve.cfg:language:disable_auto_testing "wikilink")

Переменная `disable_auto_testing` ведет себя точно так же, как
одноименная переменная секции описания задачи
[`disable_auto_testing`](serve.cfg:problem:disable_auto_testing "wikilink"),
т.е. предотвращает автоматическое тестирование посылки на заданном языке
сразу после её получения. Такая посылка получает статус "Accepted for
testing" и может быть протестирована с помощью явной команды
перетестирования посылки администратором турнира.
