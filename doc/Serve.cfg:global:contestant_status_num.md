Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Глобальные
конфигурационные
параметры](serve.cfg:global "wikilink")/[`contestant_status_num`](Serve.cfg:global:contestant_status_num "wikilink")

Дополнительный статус - это произвольная строка. Множество
дополнительных статусов участников задаётся в конфигурационном файле
турнира [`serve.cfg`](serve.cfg "wikilink"), далее на странице просмотра
и редактирования информации об участнике статус может быть изменён.
Общее количество различных статусов задаётся с помощью глобальной
конфигурационной переменной `contestant_status_num`, затем с помощью
конфигурационной переменной
[`contestant_status_legend`](serve.cfg:global:contestant_status_legend "wikilink")
должны быть заданы строки для всех статусов.
