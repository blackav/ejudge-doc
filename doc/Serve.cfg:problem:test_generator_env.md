Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[`test_generator_env`](Serve.cfg:problem:test_generator_env "wikilink")

Данная конфигурационная переменная позволяет задать дополнительные
переменные окружения, которые передаются в [программу для генерации
тестов](Программы_генерации_тестов "wikilink") на лету, которая
необходима для [динамических задач](Динамические_задачи "wikilink").

Сама программа для генерации тестов задаётся с помощью конфигурационной
переменной
[`test_generator_cmd`](Serve.cfg:problem:test_generator_cmd "wikilink").

Пример.

`[problem]`  
`#...`  
`test_generator_env = "MODE=fast"`  
`test_generator_env = "SEED=100500"`

Поддерживается с версии [3.12.0](Изменения_в_версии_3.12.0 "wikilink").
