Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[`custom_compile_cmd`](serve.cfg:problem:custom_compile_cmd "wikilink")

Данный конфигурационый параметр позволяет задавать имя скрипта
компиляции для [специальной
компиляции](специальная_компиляция "wikilink").

В турнир должен быть добавлен язык программирования `custom`. Задача, у
которой задан параметр custom_compile_cmd может быть сдана только на
этом языке программирования. Все остальные языки, разрешенные в турнире,
для нее автоматически запрещаются. Пример.

`[problem]`  
`# ...`  
`custom_compile_cmd = "compile"`  
[`custom_lang_name`](serve.cfg:problem:custom_lang_name "wikilink")` = "bash"`

Поддерживается начиная с версии
[3.10.2](изменения_в_версии_3.10.2 "wikilink").
