Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Глобальные
конфигурационные
параметры](serve.cfg:global.md)/[`sound_player`](Serve.cfg:global:sound_player.md)

|                            |                                         |     |
|----------------------------|-----------------------------------------|-----|
| **Имя переменной**:        | **`sound_player`**                      |     |
| **Содержится в:**          | [`global`](serve.cfg:global.md) |     |
| **Используется:**          | `run`                                   |     |
| **Тип содержимого:**       | *путь к файлу*                          |     |
| **Может отсутствовать:**   | *да*                                    |     |
| **Значение по умолчанию:** | *не установлено*                        |     |
| **Может повторяться:**     | *нет*                                   |     |

**Описание.** Данная конфигурационная переменная задаёт полный путь к
программе проигрывания звуковых файлов. Если переменная установлена,
программа `run` проигрывает звуковые файлы, пути к которым установлены в
конфигурационных переменных
[`accept_sound`](serve.cfg:global:accept_sound.md),
[`runtime_sound`](serve.cfg:global:runtime_sound.md),
[`timelimit_sound`](serve.cfg:global:time_limit_sound.md),
[`wrong_sound`](serve.cfg:global:wrong_sound.md),
[`presentation_sound`](serve.cfg:global:presentation_sound.md) и
[`internal_sound`](serve.cfg:global:internal_sound.md) в
зависимости от результата тестирования.

Звуковое оповещение о результате тестирования поддерживается только в
режиме турнира *ACM*.

**Пример.**

`sound_player = /usr/bin/artsplay`
