Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[`group_start_date`](serve.cfg:problem:group_start_date "wikilink")

Эта конфигурационная переменная позволяет задавать время, начиная с
которого задача становится доступной для сдачи для определенной [группы
пользователей](группа_пользователей "wikilink"). Для каждой группы
пользователей время задается в отдельной строке в формате

`@GROUP TIME`

Где `GROUP` — имя группы, а `TIME` — спецификация времени. Например,

`group_start_date = "@Group1 2010/09/01"`  
`group_start_date = "@Group2 2010/09/02 10:00:00"`

Если пользователь относится сразу к нескольким группам, то выбирается
условие, первое по списку. Если пользователь не относится ни к какой из
групп, то используеся значение конфигурационной переменной
[`start_date`](serve.cfg:problem:start_date "wikilink").

Группы, упомянутые в данной конфигурационной переменной, должны быть
загружены в турнир с помощью указания их имени в глобальной
конфигурационной переменной
[`load_user_group`](serve.cfg:global:load_user_group "wikilink").

См. также:
[`group_deadline`](serve.cfg:problem:group_deadline "wikilink"),
[`deadline`](serve.cfg:problem:deadline "wikilink"),
[`personal_deadline`](serve.cfg:problem:personal_deadline "wikilink").
