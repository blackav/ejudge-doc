Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Глобальные
конфигурационные
параметры](serve.cfg:global "wikilink")/[`compile_server_id`](Serve.cfg:global:compile_server_id "wikilink")

Данный конфигурационный параметр позволяет задать имя очереди компиляции
для компонента [ej-compile](ej-compile "wikilink"), куда по умолчанию
будут отправляться запросы на компиляцию решений.

Этот параметр аналогичен параметру
[`super_run_dir`](Serve.cfg:global:super_run_dir "wikilink"), но
работает для компиляции, а не для тестирования.

Пример:

`# global`  
`compile_server_id = "external"`

Если используется [новая схема обмена запросами с сервером
компиляции](изменения_в_версии_3.8.0 "wikilink"), то для передачи
запросов на компиляцию будет использоваться
`/home/ej-compile-spool/external`.

Поддерживается начиная с версии
[3.10.3](изменения_в_версии_3.10.3 "wikilink").
