Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[Ограничение доступа по
IP-адресам](Ограничение_доступа_по_IP-адресам "wikilink")/[Ограничения
IP-адресов в формате
XML](Ограничения_IP-адресов_в_формате_XML "wikilink")

Спецификация ограничений на IP-адрес представляет собой список
спецификаций IP-адресов, для каждого из которых указано, допустимо ли
использование CGI-программы клиентом с IP-адресом, удовлетворяющим
спецификации, или нет. Кроме этого может задаваться флаг, определяющий,
используется ли безопасное соединение по протоколу HTTPS. Элементы
списка задаются элементом [`ip`](IP:ip "wikilink") XML-файла. Описание
этого элемента дано ниже.

Для конфигурационных файлов программ
([`register`](register "wikilink")`,`[`users`](users "wikilink")`, `[`serve-control`](serve-control "wikilink")),
элементы списка находятся в элементе `access` (см. описание элемента
[`access`](register.xml:access "wikilink") конфигурационного файла
[`register.xml`](register.xml "wikilink"), описание элемента
[`access`](users.xml:access "wikilink") конфигурационного файла
[`users.xml`](users.xml "wikilink") и описание элемента access
конфигурационного файла
[`serve-control.xml`](serve-control.xml "wikilink")). Для
конфигурационного файла турнира [`contest.xml`](contest.xml "wikilink")
используются элементы
[`register_access`](contest.xml:register_access "wikilink"),
[`users_access`](contest.xml:users_access "wikilink"),
[`master_access`](contest.xml:master_access "wikilink"),
[`judge_access`](contest.xml:judge_access "wikilink"),
[`team_access`](contest.xml:team_access "wikilink"),
[`serve_control_access`](contest.xml:serve_control_access "wikilink"),
задающие дополнительные ограничения на допустимые IP-адреса для программ
[`register`](register "wikilink")`, `[`users`](users "wikilink")`, `[`master`](master "wikilink")`, `[`judge`](judge "wikilink")` и `[`team serve-control`](team_serve-control "wikilink")
соответственно. Далее даётся описание XML-элемента
[`access`](IP:access "wikilink"), справедливое для всех
вышеперечисленных элементов.

При работе CGI-программы список ограничений просматривается
последовательно от первого элемента к последнему. Как только будет
найдена первая спецификация, которой удовлетворяет IP-адрес клиента,
дальнейший просмотр прекращается и выполняется действие, указанное в
этой спецификации. Если IP-адрес клиента не удовлетворяет ни одной
спецификации, выполняется действие по умолчанию, заданное в элементе
верхнего уровня.
