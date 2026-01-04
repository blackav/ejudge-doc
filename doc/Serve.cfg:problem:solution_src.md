Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[`solution_src`](serve.cfg:problem:solution_src "wikilink")

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Abstract problems"*, поле *"Solution
source name"*, либо страница *"Editing contest"*, вкладка *"Problems
(serve.cfg)"*, блок *"Concrete problems"*, поле *"Solution source
name"*.

Данная конфигурационная переменная позволяет задавать имя файла с
исходным кодом эталонного решения задачи. Переменную следует
использовать, если для задачи определен файл заголовка (header) или
футер. Например,

`[problem]`  
`...`  
`source_header = "header.c"`  
`source_footer = "footer.c"`  
`solution_src = "root.c"`

При таких настройках полный исходный файл эталонного решения получается
объединением файлов header.c, root.c, footer.c в этом порядке. Правило
для получения полного исходного кода эталонного решения будет добавлено
в генерируемый при редактировании тестов Makefile.

Данная конфигурационная переменная поддерживается, начиная с версии
2.3.20 системы ejudge.
