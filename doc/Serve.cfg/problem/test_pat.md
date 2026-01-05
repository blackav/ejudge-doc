Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Конфигурационные
параметры
задач](serve.cfg:problem.md)/[`test_pat`](serve.cfg:problem:test_pat.md)

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Abstract problems"*, поле *"Pattern for
test file names (overrides test_suffix)"*, либо страница *"Editing
contest"*, вкладка *"Problems (serve.cfg)"*, блок *"Concrete problems"*,
поле *"Pattern for test file names (overrides test_suffix)"*.

Данная конфигурационная переменная позволяет задать шаблон имен файлов с
тестовыми данными. Шаблон записывается как спецификация преобразования
функций семейства printf языка Си.

Например,

`test_pat = "%02d"`

задает, что файлы с тестовыми данными называются `01`, `02`, `03`, ...,
`99`, `100`, `101` ...

Шаблон

`test_pat = "%03d.dat"`

задает, что файлы с тестовыми данными называются `001.dat`, `002.dat`
...

Значение конфигурационной переменной
[`test_pat`](serve.cfg:problem:test_pat.md) может определяться в
абстрактной задаче, в этом случае все конкретные задачи, относящиеся к
этой абстрактной задаче, унаследуют значение.

Если в конфигурации задачи определены и конфигурационная переменная
[`test_pat`](serve.cfg:problem:test_pat.md), и конфигурационная
переменная [`test_sfx`](serve.cfg:problem:test_sfx.md),
используется значение переменной
[`test_pat`](serve.cfg:problem:test_pat.md).
