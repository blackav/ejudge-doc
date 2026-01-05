Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Конфигурационные
параметры
задач](serve.cfg:problem.md)/[score_view](serve.cfg:problem:score_view.md)

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
