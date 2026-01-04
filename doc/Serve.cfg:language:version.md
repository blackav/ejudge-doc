Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
языков](serve.cfg:language "wikilink")/[`version`](Serve.cfg:language:version "wikilink")

Данный конфигурационный параметр позволяет указать версию языка
программирования. Он предназначен для использования в конфигурационном
файле `compile.cfg` компонента [ej-compile](ej-compile "wikilink"). Он
полезен, чтобы отделить версию компилятора от названия компилятора.
Например,

`[language]`  
`id = 52`  
`short_name = "clang++"`  
`long_name = "clang C++"`  
`arch = "linux-shared"`  
`src_sfx = ".cpp"`  
`cmd = "clang++"`  
`version = "18.1.8"`

Поддерживается начиная с версии
[3.13.0](изменения_в_версии_3.13.0 "wikilink").
