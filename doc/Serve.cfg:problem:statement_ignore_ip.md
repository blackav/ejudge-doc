Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[`statement_ignore_ip`](Serve.cfg:problem:statement_ignore_ip "wikilink")

Если данная конфигурационная переменная установлена в положительное
значение, на отображение условия задачи в интерфейсе участника турнира
не действуют ограничения, накладываемые конфигурационной переменной
[`allow_ip`](serve.cfg:problem:allow_ip "wikilink").

Значение переменной наследуется из абстрактной задачи.

Пример:

`[problem]`  
`# ...`  
[`allow_ip`](serve.cfg:problem:allow_ip "wikilink")` = "1.2.3.4"`  
`allow_ip = "10.0.0.0/8"`  
`allow_ip = "192.168.99.0/24"`  
`statement_ignore_ip`

Поддерживается начиная с версии
[3.12.0](изменения_в_версии_3.12.0 "wikilink").
