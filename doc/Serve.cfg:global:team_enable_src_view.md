Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Глобальные
конфигурационные
параметры](serve.cfg:global "wikilink")/[`team_enable_src_view`](Serve.cfg:global:team_enable_src_view "wikilink")

|                            |                                         |     |
|----------------------------|-----------------------------------------|-----|
| **Имя переменной**:        | **`team_enable_src_view`**              |     |
| **Содержится в:**          | [`global`](serve.cfg:global "wikilink") |     |
| **Используется:**          | `serve`                                 |     |
| **Тип содержимого:**       | *boolean*                               |     |
| **Может отсутствовать:**   | *да*                                    |     |
| **Значение по умолчанию:** | *false*                                 |     |
| **Может повторяться:**     | *нет*                                   |     |

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Global settings (serve.cfg)"*, блок *"Contestant's capabilities"*,
поле *"Contestant may view submitted source code"*.

**Описание.** Если данная конфигурационная переменная установлена в
*true*, участники турнира получают возможность просматривать текст
программ, посланных ими на проверку и хранящихся в базе данных системы
`ejudge`.

**Пример.**

`team_enable_src_view`
