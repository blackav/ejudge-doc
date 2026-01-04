Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[`init_env`](Serve.cfg:problem:init_env "wikilink")

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Abstract problems"*, поле *"Init-style
interactor name"*, либо страница *"Editing contest"*, вкладка *"Problems
(serve.cfg)"*, блок *"Concrete problems"*, поле *"Init-style interactor
environment"*.

Данная конфигурационная переменная позволяет задать переменные окружения
для [программы инициализации](программы_инициализации "wikilink").

Значение переменной наследуется из абстрактной задачи.

Пример:

`[problem]`  
`# ...`  
`init_env = "VAR1=value1"`  
`init_env = "VAR2=value2"`

Конфигурационная переменная поддерживается, начиная с версии
[2.3.22](изменения_в_версии_2.3.22 "wikilink").
