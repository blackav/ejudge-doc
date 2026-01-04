Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Конфигурационные
параметры
задач](serve.cfg:problem.md)/[enable_compilation](serve.cfg:problem:enable_compilation.md)

Переменная действует только тогда, когда для задачи установлена
переменная
[`disable_testing`](serve.cfg:problem:disable_testing.md). Если
в этом случае переменная `enable_compilation` установлена в 1, то
присланные решения по этой задаче компилируются. Если компиляция
завершилась успешно, то для посылки устанавливается статус "Accepted for
testing" (`RUN_ACCEPTED`), а в противном случае устанавливается статус
"Compilation error" (`RUN_COMPILE_ERR`).
