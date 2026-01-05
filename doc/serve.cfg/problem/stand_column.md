Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Конфигурационные
параметры
задач](serve.cfg:problem.md)/[stand_column](serve.cfg:problem:stand_column.md)

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Concrete problems"*, поле *"Collate
this problem with the specified one"*.

Данная переменная позволяет отображать результаты по данной задаче в
столбце, относящемся к другой задаче, имя которой задается в значении
переменной. Столбец, относящийся к задаче с установленным значением
`stand_column`, не показывается. Значением `stand_column` должно быть
либо значение [`stand_name`](serve.cfg:problem:stand_name.md),
либо значение [`short_name`](serve.cfg:problem:short_name.md)
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
