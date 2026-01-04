Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[`init_cmd`](Serve.cfg:problem:init_cmd "wikilink")

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Abstract problems"*, поле *"Init-style
interactor name"*, либо страница *"Editing contest"*, вкладка *"Problems
(serve.cfg)"*, блок *"Concrete problems"*, поле *"Init-style interactor
name"*.

Данная конфигурационная переменная позволяет задать имя для [программы
инициализации](программы_инициализации "wikilink").

Если указан относительный путь, то полный путь к программе инициализации
строится по тем же правилам, по которым путь к проверяющей программе.

Значение переменной наследуется из абстрактной задачи.

Пример:

`[problem]`  
`# ...`  
`init_cmd = "init_A"`

Конфигурационная переменная поддерживается, начиная с версии
[2.3.22](изменения_в_версии_2.3.22 "wikilink").
