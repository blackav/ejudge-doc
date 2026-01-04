Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Глобальные
конфигурационные
параметры](serve.cfg:global "wikilink")/[`ignore_compile_errors`](Serve.cfg:global:ignore_compile_errors "wikilink")

|                            |                                         |     |
|----------------------------|-----------------------------------------|-----|
| **Имя переменной**:        | **`ignore_compile_errors`**             |     |
| **Содержится в:**          | [`global`](serve.cfg:global "wikilink") |     |
| **Используется:**          | `serve`                                 |     |
| **Тип содержимого:**       | *boolean*                               |     |
| **Может отсутствовать:**   | *да*                                    |     |
| **Значение по умолчанию:** | *false*                                 |     |
| **Может повторяться:**     | *нет*                                   |     |

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Global settings (serve.cfg)"*, блок *"Contestant's capabilities"*,
поле *"Compilation errors are not counted as failed runs"*.

**Описание.** Если значение данной конфигурационной переменной равно
*true*, если программа, посланная участником, не может быть
скомпилирована (например, из-за синтаксических ошибок), такая программа
не засчитывается, то есть за неё не начисляется штраф.

**Пример.**

`ignore_compile_errors`

Смотри также
[`compile_error_penalty`](serve.cfg:problem:compile_error_penalty "wikilink").
