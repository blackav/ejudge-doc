Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[`corr_pat`](serve.cfg:problem:corr_pat "wikilink")

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Abstract problems"*, поле *"Pattern for
"correct answer" file names (overrides corr_suffix)"*, либо страница
*"Editing contest"*, вкладка *"Problems (serve.cfg)"*, блок *"Concrete
problems"*, поле *"Pattern for "correct answer" file names (overrides
corr_suffix)"*.

Данная конфигурационная переменная позволяет задать шаблон имен файлов с
эталонными ответами. Шаблон записывается как спецификация преобразования
функций семейства printf языка Си.

Например,

`corr_pat = "%02d.a"`

задает, что файлы с эталонными ответами называются `01.a`, `02.a`,
`03.a`, ..., `99.a`, `100.a`, `101.a` ...

Шаблон

`corr_pat = "%03d.ans"`

задает, что файлы с эталонными ответами называются `001.ans`, `002.ans`
...

Значение конфигурационной переменной
[`corr_pat`](serve.cfg:problem:corr_pat "wikilink") может определяться в
абстрактной задаче, в этом случае все конкретные задачи, относящиеся к
этой абстрактной задаче, унаследуют значение.

Если в конфигурации задачи определены и конфигурационная переменная
[`corr_pat`](serve.cfg:problem:corr_pat "wikilink"), и конфигурационная
переменная [`corr_sfx`](serve.cfg:problem:corr_sfx "wikilink"),
используется значение переменной
[`corr_pat`](serve.cfg:problem:corr_pat "wikilink").
