Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[stand_column](serve.cfg:problem:stand_column "wikilink")

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Concrete problems"*, поле *"Collate
this problem with the specified one"*.

Данная переменная позволяет отображать результаты по данной задаче в
столбце, относящемся к другой задаче, имя которой задается в значении
переменной. Столбец, относящийся к задаче с установленным значением
`stand_column`, не показывается. Значением `stand_column` должно быть
либо значение [`stand_name`](serve.cfg:problem:stand_name "wikilink"),
либо значение [`short_name`](serve.cfg:problem:short_name "wikilink")
некоторой другой задачи, у которой не должна быть установлена
`stand_column`.

**Пример.**

`[problem]`  
`short_name = "A-1"`  
`stand_name = "A"`  
  
`[problem]`  
`short_name = "A-2"`  
`stand_column = "A"`  
  
`[problem]`  
`short_name = "A-3"`  
`stand_column = "A"`

Результаты по задачам "A-1", "A-2" и "A-3" будут отображены в столбце
"A". Отдельных столбцов для "A-2" и "A-3" в таблице не будет.
