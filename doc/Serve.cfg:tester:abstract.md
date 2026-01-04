Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
тестирования](serve.cfg:tester "wikilink")/[abstract](Serve.cfg:tester:abstract "wikilink")

|                            |                                         |
|----------------------------|-----------------------------------------|
| **Имя переменной**:        | **`abstract`**                          |
| **Содержится в:**          | [`tester`](serve.cfg:tester "wikilink") |
| **Используется:**          | `serve, run`                            |
| **Тип содержимого:**       | *boolean*                               |
| **Может отсутствовать:**   | *да*                                    |
| **Наследуется:**           | *нет*                                   |
| **Значение по умолчанию:** | `false`                                 |
| **Может повторяться:**     | *нет*                                   |

**Описание.** Если данная конфигурационная переменная установлена в
*true*, текущее описание тестировщика является описанием абстрактного
тестировщика.

Абстрактный тестировщик не имеет идентификатора (то есть не может
использовать параметр [`id`](serve.cfg:tester:id "wikilink")), не может
быть тестировщиком по умолчанию (то есть не может устанавливать параметр
`any`), не может устанавливать тестируемую задачу с помощью
конфигурационных переменных
[`problem`](serve.cfg:tester:problem "wikilink") или
[`problem_name`](serve.cfg:tester:problem_name "wikilink"). Абстрактный
тестировщик не может наследовать свойства другого абстрактного
тестировщика, то есть использование конфигурационной переменной
[`super`](serve.cfg:tester:super "wikilink") в описании абстрактного
тестировщика не допускается.

Описание абстрактного тестировщика должно устанавливать параметр
[`name`](serve.cfg:tester:name "wikilink"), который используется для
идентификации абстрактного тестировщика. Имя абстрактного тестировщика
должно быть уникальным среди всех абстрактных тестировщиков.

Описание абстрактного тестировщика устанавливает значения
конфигурационных переменных. Неабстрактный тестировщик указывает имя
абстрактного тестировщика в конфигурационной переменной
[`super`](serve.cfg:tester:super "wikilink"), при этом значение
некоторой переменной наследуется из абстрактного тестировщика только в
том случае, если эта переменная не установлена в самом неабстрактном
тестировщике.

Конкретный тестировщик может наследовать следующие конфигурационные
переменные из описания абстрактного тестировщика:
[`arch`](serve.cfg:tester:arch "wikilink"),
[`check_cmd`](serve.cfg:tester:check_cmd "wikilink"),
[`check_dir`](serve.cfg:tester:check_dir "wikilink"),
[`clear_env`](serve.cfg:tester:clear_env "wikilink"),
[`errorcode_file`](serve.cfg:tester:errorcode_file "wikilink"),
[`error_file`](serve.cfg:tester:error_file "wikilink"),
[`is_dos`](serve.cfg:tester:is_dos "wikilink"),
[`key`](serve.cfg:tester:key "wikilink"),
[`kill_signal`](serve.cfg:tester:kill_signal "wikilink"),
[`max_data_size`](serve.cfg:tester:max_data_size "wikilink"),
[`max_stack_size`](serve.cfg:tester:max_stack_size "wikilink"),
[`max_vm_size`](serve.cfg:tester:max_vm_size "wikilink"),
[`no_core_dump`](serve.cfg:tester:no_core_dump "wikilink"),
[`no_redirect`](serve.cfg:tester:no_redirect "wikilink"),
[`prepare_cmd`](serve.cfg:tester:prepare_cmd "wikilink"),
[`run_dir`](serve.cfg:tester:run_dir "wikilink"),
[`start_cmd`](serve.cfg:tester:start_cmd "wikilink"),
[`start_env`](serve.cfg:tester:start_env "wikilink"),
[`time_limit_adjustment`](serve.cfg:tester:time_limit_adjustment "wikilink").

При этом при наследовании конфигурационных переменных
[`check_cmd`](serve.cfg:tester:check_cmd "wikilink"),
[`check_dir`](serve.cfg:tester:check_dir "wikilink"),
[`errorcode_file`](serve.cfg:tester:errorcode_file "wikilink"),
[`error_file`](serve.cfg:tester:error_file "wikilink"),
[`prepare_cmd`](serve.cfg:tester:prepare_cmd "wikilink"),
[`run_dir`](serve.cfg:tester:run_dir "wikilink"),
[`start_cmd`](serve.cfg:tester:start_cmd "wikilink") выполняется
[форматная подстановка](форматная_подстановка "wikilink").

**Не наследуются** следующие конфигурационные переменные абстрактной
задачи: [`abstract`](serve.cfg:tester:abstract "wikilink"),
[`any`](serve.cfg:tester:any "wikilink"),
[`id`](serve.cfg:tester:id "wikilink"),
[`name`](serve.cfg:tester:name "wikilink"),
[`problem`](serve.cfg:tester:problem "wikilink"),
[`problem_name`](serve.cfg:tester:problem_name "wikilink"),
[`super`](serve.cfg:tester:super "wikilink").

**Пример.**

`abstract`
