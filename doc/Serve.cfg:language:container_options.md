Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
языков](serve.cfg:language "wikilink")/[`container_options`](Serve.cfg:language:container_options "wikilink")

Эта конфигурационная переменная позволяет задать дополнительные опции
для программы контейнеризации
[ej-suid-container](ej-suid-container "wikilink") для выполнения
программ, скомпилированных данным языком программирования. Опция
действует только когда [разрешен запуск в
контейнере](Изоляция_недоверенных_процессов_в_контейнерах "wikilink").
Дополнительные опции дописываются в конец параметра опций строки запуска
контейнера.

Пример:

`[language]`  
`# ...`  
`container_options = "mh"`

Для изменения опций контейнеризации для компилятора языка, используйте
[`compiler_container_options`](Serve.cfg:language:compiler_container_options "wikilink").

Поддерживается начиная с версии
[3.9.0](изменения_в_версии_3.9.0 "wikilink").
