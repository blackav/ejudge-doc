Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
языков](serve.cfg:language "wikilink")/[`run_max_rss_size`](Serve.cfg:language:run_max_rss_size "wikilink")

Эта конфигурационная переменная позволяет задать ограничение на
максимальный размер использованной оперативной памяти (resident set
size - RSS) для тестирования программ на этом языке программирования.
Эта конфигурационная переменная имеет приоритет над переменной задач
[`max_rss_size`](Serve.cfg:problem:max_rss_size "wikilink").

Опция имеет эффект только тогда, когда [разрешен запуск тестируемых
программ в
контейнере](Изоляция_недоверенных_процессов_в_контейнерах "wikilink"). В
противном случае она игнорируется.

См. также [`max_rss_size`](serve.cfg:problem:max_rss_size "wikilink"),
[`lang_max_rss_size`](serve.cfg:problem:lang_max_rss_size "wikilink").

Пример.

`[language]`  
`# ...`  
`run_max_rss_size = 1G`

Поддерживается начиная с версии
[3.9.0](изменения_в_версии_3.9.0 "wikilink").
