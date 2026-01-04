Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[enable_compilation](serve.cfg:problem:enable_compilation "wikilink")

Переменная действует только тогда, когда для задачи установлена
переменная
[`disable_testing`](serve.cfg:problem:disable_testing "wikilink"). Если
в этом случае переменная `enable_compilation` установлена в 1, то
присланные решения по этой задаче компилируются. Если компиляция
завершилась успешно, то для посылки устанавливается статус "Accepted for
testing" (`RUN_ACCEPTED`), а в противном случае устанавливается статус
"Compilation error" (`RUN_COMPILE_ERR`).
