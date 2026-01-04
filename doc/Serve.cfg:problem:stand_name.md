Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[stand_name](serve.cfg:problem:stand_name "wikilink")

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Concrete problems"*, поле *"Title for
the standings column"*.

Данная переменная позволяет задавать название столбца задачи в таблице
текущих результатов турнира. Если переменная не определена, то в
качестве названия столбца используется короткое имя задачи
[`short_name`](serve.cfg:problem:short_name "wikilink").

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
"A". Отдельных столбцов для "A-2" и "A-3" в таблице не будет. Переменной
`stand_name` соответствует форматная подстановка %PS.
