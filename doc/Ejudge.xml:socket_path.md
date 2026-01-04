Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[ejudge.xml](ejudge.xml "wikilink")/[`socket_path`](ejudge.xml:socket_path "wikilink")

|                            |                                                                                                                                                                                                                                                                                                                                                                        |     |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
| **Имя элемента**:          | **`socket_path`**                                                                                                                                                                                                                                                                                                                                                      |     |
| **Содержится в:**          | [`config`](ejudge.xml:config "wikilink")                                                                                                                                                                                                                                                                                                                               |     |
| **Может содержать:**       | *нет*                                                                                                                                                                                                                                                                                                                                                                  |     |
| **Атрибуты:**              | *нет*                                                                                                                                                                                                                                                                                                                                                                  |     |
| **Тип содержимого:**       | путь к UNIX-сокету                                                                                                                                                                                                                                                                                                                                                     |     |
| **Значение по умолчанию:** | задается скриптом [`configure`](configure "wikilink")                                                                                                                                                                                                                                                                                                                  |     |
| **Может отсутствовать:**   | *да*                                                                                                                                                                                                                                                                                                                                                                   |     |
| **Может повторяться:**     | *нет*                                                                                                                                                                                                                                                                                                                                                                  |     |
| **Используется в:**        | [`edit-userlist`](edit-userlist "wikilink"), [`judge`](judge "wikilink"), [`master`](master "wikilink"), [`register`](register "wikilink"), [`serve`](serve "wikilink"), [`serve-control`](serve-control "wikilink"), [`super-serve`](super-serve "wikilink"), [`team`](team "wikilink"), [`userlist-server`](userlist-server "wikilink"), [`users`](users "wikilink") |     |
| **Примечание:**            | явное использование не рекомендуется                                                                                                                                                                                                                                                                                                                                   |     |

**Описание.** Данный элемент задаёт путь к UNIX-сокету, который
используется для связи с сервером информации о пользователях
[`userlist-server`](userlist-server "wikilink"). Сокет создаётся при
старте этой программы, поэтому должен находится в каталоге, доступном ей
на запись. Смотри также элемент `socket_path` конфигурационного файла
`users.xml`, элемент `socket_path` конфигурационного файла
`register.xml`, параметр `socket_path` конфигурационного файла
`master.cfg`, параметр `socket_path` конфигурационного файла
[`judge.cfg`](judge.cfg "wikilink"), параметр `socket_path`
конфигурационного файла [`team.cfg`](team.cfg "wikilink"), параметр
[`socket_path`](Serve.cfg:global:socket_path "wikilink")
конфигурационного файла [`serve.cfg`](serve.cfg "wikilink").

Рекомендуется при компиляции системы указывать путь к сокету с помощью
опции `-- enable-socket-path` скрипта
[`configure`](configure "wikilink"). Тогда указанный путь будет
использоваться как путь по умолчанию, и может не устанавливаться явно в
конфигурационных файлах. Поэтому явное использование тега `socket_path`
не рекомендуется.

**Пример.**

<socket_path>`/var/ejudge/userlist-socket`</socket_path>
