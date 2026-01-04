Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[contest.xml](contest.xml "wikilink")/[register_url](contest.xml:register_url "wikilink")

|                          |                                             |
|--------------------------|---------------------------------------------|
| **Имя элемента**:        | **`register_url`**                          |
| **Содержится в:**        | [`contest`](contest.xml:contest "wikilink") |
| **Может содержать:**     | *нет*                                       |
| **Атрибуты:**            | *нет*                                       |
| **Тип содержимого:**     | URL                                         |
| **Может отсутствовать:** | *да*                                        |
| **Может повторяться:**   | *нет*                                       |

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"General settings (contest.xml)"*, блок *"Registration settings"*, поле
*"URL to complete registration"*.

**Описание.** Данный элемент позволяет задать URL CGI-программы
[`register`](register "wikilink") для дальнейшей регистрации в системе
`ejudge`. Этот URL будет помещён в текст письма-уведомления, посылаемого
пользователю при регистрации в системе. Если в конфигурационном файле
турнира [`contest.xml`](contest.xml "wikilink") данный элемент не задан,
используется URL, заданный в элементе
[`register_url`](ejudge.xml:register_url "wikilink") конфигурационного
файла [`ejudge.xml`](ejudge.xml "wikilink"). Если и тот элемент не
задан, используется URL по умолчанию
`http://contest.cmc.msu.ru/cgi-bin/register`. К URL, заданному в любом
из конфигурационных файлов или по умолчанию, автоматически добавляется
параметр `contest_id` со значением, равным идентификатору данного
турнира, параметр `locale_id` со значением, равным идентификатору
выбранного языка интерфейса, параметр `login` со значением, равным
регистрационному имени нового пользователя, и параметр `action` со
значением 3 для перехода непосредственно к странице входа в систему.
Таким образом, полностью сформированный URL для примера ниже может
выглядеть следующим образом

http://www.supercontest.ru/cgi-bin/register?action=3&login=user&contest_id=4&locale_id=1

**Пример.**

`<register_url>http://www.supercontest.ru/cgi-bin/register</register_url>`
