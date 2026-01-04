Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Глобальные
конфигурационные
параметры](serve.cfg:global "wikilink")/[`contestant_status_legend`](Serve.cfg:global:contestant_status_legend "wikilink")

Дополнительный статус - это произвольная строка. Множество
дополнительных статусов участников задаётся в конфигурационном файле
турнира [`serve.cfg`](serve.cfg "wikilink"), далее на странице просмотра
и редактирования информации об участнике статус может быть изменён.
Общее количество различных статусов задаётся с помощью глобальной
конфигурационной переменной
[`contestant_status_num`](serve.cfg:global:contestant_status_num "wikilink"),
затем с помощью конфигурационной переменной `contestant_status_legend`
должны быть заданы строки для всех статусов.

Первый статус получает номер 0, второй - 1 и т. д. Каждый участник
турнира получит статус по умолчанию, равный 0, который затем может быть
изменён.

Пример задания статусов:

`contestant_status_num = 3`  
`contestant_status_legend = "Status 0"`  
`contestant_status_legend = "Status 1"`  
`contestant_status_legend = "Status 2"`
