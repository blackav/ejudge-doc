Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[score_view](serve.cfg:problem:score_view "wikilink")

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Abstract problems"*, поле *"Solution
command"*, либо страница *"Editing contest"*, вкладка *"Problems
(serve.cfg)"*, блок *"Concrete problems"*, поле *"Special view for
scores"*.

Эта переменная позволяет задавать отображение числовых баллов за задачу
в символьные строки. Например,

`score_view = "0 0"`  
`score_view = "1 -"`  
`score_view = "2 +"`

задаёт, что 0 баллов будет отображаться как "0", 1 балл - как "-", а 2
балла - как "+".
