Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[team.cfg](team.cfg "wikilink")

Данный конфигурационный файл используется CGI-программой
[`team`](team "wikilink"). Содержимое файла прочитывается один раз при
старте CGI-программы, то есть каждый раз, когда кто-либо посылает
HTTP/HTTPS-запрос к серверу, приводящий к запуску программы `team`.
[Подробнее...](team.cfg:info "wikilink")

Конфигурационный файл `team.cfg` имеет текстовый формат, напоминающий
формат `.ini`-файлов. Каждый конфигурационный параметр задаётся в виде

<имя параметра>` = `<значение>

где <имя параметра> может состоять из латинских заглавных и строчных
букв, цифр и знака подчёркивания. <значение> должно заключаться в
кавычки, если оно содержит пробельные символы, но может быть задано и
без кавычек, если оно состоит из единственного слова. Пробельные символы
в начале и конце строки и вокруг знака `-"` игнорируются.

Комментарии в конфигурационном файле начинаются с символов `#` или `;` и
продолжаются до конца строки.

Параметры конфигурационного файла:

- [allow_deny](team.cfg:allow_deny "wikilink")
- [allow_from](team.cfg:allow_from "wikilink")
- [deny_from](team.cfg:deny_from "wikilink")
- [charset](team.cfg:charset "wikilink")
- [enable_l10n](team.cfg:enable_l10n "wikilink")
- [l10n_dir](team.cfg:l10n_dir "wikilink")
- [socket_path](team.cfg:socket_path "wikilink")
- [contests_dir](team.cfg:contests_dir "wikilink")
- [show_generation_time](team.cfg:show_generation_time "wikilink")
