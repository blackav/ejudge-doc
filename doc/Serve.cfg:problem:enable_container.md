Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[`enable_container`](Serve.cfg:problem:enable_container "wikilink")

Если данная конфигурационная переменная задачи установлена в 1, для
запуска решений для данной задачи будет использоваться [механизм
контейнеров](Изоляция_недоверенных_процессов_в_контейнерах "wikilink").
Если конфигурационная переменная установлена в 0, для запуска решений
будут использоваться старые механизмы ([патч к ядру
Linux](патч_к_ядру_Linux "wikilink"), [тестирование под отдельным
пользователем](тестирование_под_отдельным_пользователем "wikilink")).

Однако, если в конфигурационном файле `ejudge.xml` установлен атрибут
`force_container`, то для запуска всех решений всегда будет
использоваться механизм контейнеров, и это нельзя отключить.

Механизм запуска в контейнерах отключает действие следующих
конфигурационных переменных языка программирования:
[`disable_security`](serve.cfg:language:disable_security "wikilink"),
[`insecure`](serve.cfg:language:insecure "wikilink").

Механизм запуска в контейнерах отключает действие следующих
конфигурационных переменных задачи:
[`disable_security`](serve.cfg:problem:disable_security "wikilink"),
[`enable_kill_all`](serve.cfg:problem:enable_kill_all "wikilink"),
[`enable_process_group`](serve.cfg:problem:enable_process_group "wikilink"),
[`enable_suid_run`](serve.cfg:problem:enable_suid_run "wikilink").

Значение данной конфигурационной переменной наследуется из абстрактной
задачи, если оно определено в абстрактной задаче и не переопределено в
конкретной задаче.

Поддерживается начиная с версии
[3.9.0](изменения_в_версии_3.9.0 "wikilink").
