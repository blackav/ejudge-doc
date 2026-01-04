Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[`max_rss_size`](Serve.cfg:problem:max_rss_size "wikilink")

Эта конфигурационная переменная позволяет задать ограничение на
максимальный размер использованной оперативной памяти (resident set
size - RSS) для решений данной задачи.

Опция имеет эффект только тогда, когда [разрешен запуск компиляторов в
контейнере](Изоляция_недоверенных_процессов_в_контейнерах "wikilink"). В
противном случае она игнорируется.

См. также
[`lang_max_rss_size`](serve.cfg:problem:lang_max_rss_size "wikilink"),
[`max_rss_size`](serve.cfg:language:max_rss_size "wikilink").

Пример.

`[problem]`  
`# ...`  
`max_rss_size = 256M`

Поддерживается начиная с версии
[3.9.0](изменения_в_версии_3.9.0 "wikilink").
