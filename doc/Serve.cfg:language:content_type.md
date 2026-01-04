Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
языков](serve.cfg:language "wikilink")/[content_type](Serve.cfg:language:content_type "wikilink")

Если эта переменная установлена, то по команде "Download source"
CGI-программ `master` или `judge` или по команде "View source" будет
генерироваться страница с указанным значением поля "Content-Type". Это
поле полезно для "языков" с бинарным представлением. Например, если в
системе есть язык "Microsoft Word", то для него можно установить поле
`content_type` так:

`content_type = "application/msword"`
