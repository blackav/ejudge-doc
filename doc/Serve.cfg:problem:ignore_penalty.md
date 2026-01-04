Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Конфигурационные
параметры
задач](serve.cfg:problem.md)/[ignore_penalty](serve.cfg:problem:ignore_penalty.md)

Переменная работает только для турниров *OLYMPIAD* в режиме, задаваемом
глобальной конфигурационной переменной
[`stand_enable_penalty`](serve.cfg:global:stand_enable_penalty.md).
Если значение переменной `ignore_penalty` не равно 0, то для данной
задачи штрафные баллы всегда будут равны 0, независимо от времени её
сдачи.
