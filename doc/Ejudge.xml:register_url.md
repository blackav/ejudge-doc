Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[ejudge.xml](ejudge.xml "wikilink")/[`register_url`](ejudge.xml:register_url "wikilink")

|                          |                                                 |     |
|--------------------------|-------------------------------------------------|-----|
| **Имя элемента**:        | **`register_url`**                              |     |
| **Содержится в:**        | [`config`](ejudge.xml:config "wikilink")        |     |
| **Может содержать:**     | *нет*                                           |     |
| **Атрибуты:**            | *нет*                                           |     |
| **Тип содержимого:**     | URL                                             |     |
| **Может отсутствовать:** | *да*                                            |     |
| **Может повторяться:**   | *нет*                                           |     |
| **Используется в:**      | [`userlist-server`](userlist-server "wikilink") |     |

**Описание.** Данный элемент задаёт URL CGI программы
[`register`](register "wikilink"), которая отвечает за регистрацию новых
пользователей, изменение пользователями своих персональных данных и
регистрацию пользователей на турниры. Этот URL добавляется в текст
уведомления о регистрации. Если этот элемент не определён, используется
URL по умолчанию
[`http://contest.cmc.msu.ru/cgi-bin/register`](http://contest.cmc.msu.ru/cgi-bin/register).
Значение, устанавливаемое этим элементом может быть переопределено
элементом [`register_url`](contest.xml:register_url "wikilink")
конфигурационного файла турнира [`contest.xml`](contest.xml "wikilink").

**Пример.**

<register_url>[`http://www.olympiads.ru/cgi-bin/register`](http://www.olympiads.ru/cgi-bin/register)</register_url>
