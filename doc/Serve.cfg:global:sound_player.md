Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Глобальные
конфигурационные
параметры](serve.cfg:global "wikilink")/[`sound_player`](Serve.cfg:global:sound_player "wikilink")

|                            |                                         |     |
|----------------------------|-----------------------------------------|-----|
| **Имя переменной**:        | **`sound_player`**                      |     |
| **Содержится в:**          | [`global`](serve.cfg:global "wikilink") |     |
| **Используется:**          | `run`                                   |     |
| **Тип содержимого:**       | *путь к файлу*                          |     |
| **Может отсутствовать:**   | *да*                                    |     |
| **Значение по умолчанию:** | *не установлено*                        |     |
| **Может повторяться:**     | *нет*                                   |     |

**Описание.** Данная конфигурационная переменная задаёт полный путь к
программе проигрывания звуковых файлов. Если переменная установлена,
программа `run` проигрывает звуковые файлы, пути к которым установлены в
конфигурационных переменных
[`accept_sound`](serve.cfg:global:accept_sound "wikilink"),
[`runtime_sound`](serve.cfg:global:runtime_sound "wikilink"),
[`timelimit_sound`](serve.cfg:global:time_limit_sound "wikilink"),
[`wrong_sound`](serve.cfg:global:wrong_sound "wikilink"),
[`presentation_sound`](serve.cfg:global:presentation_sound "wikilink") и
[`internal_sound`](serve.cfg:global:internal_sound "wikilink") в
зависимости от результата тестирования.

Звуковое оповещение о результате тестирования поддерживается только в
режиме турнира *ACM*.

**Пример.**

`sound_player = /usr/bin/artsplay`
