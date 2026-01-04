Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Конфигурационные
параметры
задач](serve.cfg:problem.md)/[`compile_error_penalty`](serve.cfg:problem:compile_error_penalty.md)

Данная конфигурационная переменная позволяет задавать штраф за ошибки
компиляции. Переменная действует, если отключен режим
[`ignore_compile_errors`](serve.cfg:problem:ignore_compile_errors.md),

`compile_error_penalty = 1`

Конфигурационная переменная наследуется из абстрактной задачи.

Поддерживается с версии [3.6.1](изменения_в_версии_3.6.1.md).
