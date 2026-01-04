Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[ignore_penalty](serve.cfg:problem:ignore_penalty "wikilink")

Переменная работает только для турниров *OLYMPIAD* в режиме, задаваемом
глобальной конфигурационной переменной
[`stand_enable_penalty`](serve.cfg:global:stand_enable_penalty "wikilink").
Если значение переменной `ignore_penalty` не равно 0, то для данной
задачи штрафные баллы всегда будут равны 0, независимо от времени её
сдачи.
