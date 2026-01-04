Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Глобальные
конфигурационные
параметры](serve.cfg:global "wikilink")/[`extra_compile_dirs`](Serve.cfg:global:extra_compile_dirs "wikilink")

С помощью данной переменной указываются каталоги обмена для серверов
компиляции.

Например,

`extra_compile_dirs = "win32_compile"`  
`extra_compile_dirs = "compile2"`

указывает, что каталог обмена с сервером компиляции с номером 1
называется `CONTESTS_HOME_DIR/win32_compile/var/compile`, а каталог
обмена с сервером компиляции с номером 2 называется
`CONTESTS_HOME_DIR/compile2/var/compile`

Сервер компиляции с номером 0 - это основной сервер компиляции, каталог
обмена которого указывается в переменной
[`compile_dir`](serve.cfg:global:compile_dir "wikilink").
