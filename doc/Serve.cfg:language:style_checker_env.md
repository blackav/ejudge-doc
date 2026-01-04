Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
языков](serve.cfg:language "wikilink")/[style_checker_env](Serve.cfg:language:style_checker_env "wikilink")

Данная конфигурационная переменная позволяет задавать переменные
окружения, передаваемые [программе проверки
стиля](style_checkers "wikilink"). Если у соответствующего языка
программирования указана переменная
[`style_checker_cmd`](Serve.cfg:language:style_checker_cmd "wikilink"),
то переменные окружения будут переданы в эту программу.

Данная конфигурационная переменная может быть указана в разделе описания
языка несколько раз, задавая каждый раз новую переменную окружения.

Пример определения переменной:

`style_checker_env = "EJ_TESTS_MODE=1"`  
`style_checker_env = "EJ_MAX_FILE_SIZE=1K"`  
`style_checker_env = "EJ_MAX_TEST_COUNT=10"`
