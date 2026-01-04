Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Конфигурационные
параметры
языков](serve.cfg:language.md)/[content_type](Serve.cfg:language:content_type.md)

Если эта переменная установлена, то по команде "Download source"
CGI-программ `master` или `judge` или по команде "View source" будет
генерироваться страница с указанным значением поля "Content-Type". Это
поле полезно для "языков" с бинарным представлением. Например, если в
системе есть язык "Microsoft Word", то для него можно установить поле
`content_type` так:

`content_type = "application/msword"`
