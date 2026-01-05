Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Конфигурационные
параметры
тестирования](serve.cfg:tester.md)/[abstract](Serve.cfg:tester:abstract.md)

|                            |                                         |
|----------------------------|-----------------------------------------|
| **Имя переменной**:        | **`abstract`**                          |
| **Содержится в:**          | [`tester`](serve.cfg:tester.md) |
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
использовать параметр [`id`](serve.cfg:tester:id.md)), не может
быть тестировщиком по умолчанию (то есть не может устанавливать параметр
`any`), не может устанавливать тестируемую задачу с помощью
конфигурационных переменных
[`problem`](serve.cfg:tester:problem.md) или
[`problem_name`](serve.cfg:tester:problem_name.md). Абстрактный
тестировщик не может наследовать свойства другого абстрактного
тестировщика, то есть использование конфигурационной переменной
[`super`](serve.cfg:tester:super.md) в описании абстрактного
тестировщика не допускается.

Описание абстрактного тестировщика должно устанавливать параметр
[`name`](serve.cfg:tester:name.md), который используется для
идентификации абстрактного тестировщика. Имя абстрактного тестировщика
должно быть уникальным среди всех абстрактных тестировщиков.

Описание абстрактного тестировщика устанавливает значения
конфигурационных переменных. Неабстрактный тестировщик указывает имя
абстрактного тестировщика в конфигурационной переменной
[`super`](serve.cfg:tester:super.md), при этом значение
некоторой переменной наследуется из абстрактного тестировщика только в
том случае, если эта переменная не установлена в самом неабстрактном
тестировщике.

Конкретный тестировщик может наследовать следующие конфигурационные
переменные из описания абстрактного тестировщика:
[`arch`](serve.cfg:tester:arch.md),
[`check_cmd`](serve.cfg:tester:check_cmd.md),
[`check_dir`](serve.cfg:tester:check_dir.md),
[`clear_env`](serve.cfg:tester:clear_env.md),
[`errorcode_file`](serve.cfg:tester:errorcode_file.md),
[`error_file`](serve.cfg:tester:error_file.md),
[`is_dos`](serve.cfg:tester:is_dos.md),
[`key`](serve.cfg:tester:key.md),
[`kill_signal`](serve.cfg:tester:kill_signal.md),
[`max_data_size`](serve.cfg:tester:max_data_size.md),
[`max_stack_size`](serve.cfg:tester:max_stack_size.md),
[`max_vm_size`](serve.cfg:tester:max_vm_size.md),
[`no_core_dump`](serve.cfg:tester:no_core_dump.md),
[`no_redirect`](serve.cfg:tester:no_redirect.md),
[`prepare_cmd`](serve.cfg:tester:prepare_cmd.md),
[`run_dir`](serve.cfg:tester:run_dir.md),
[`start_cmd`](serve.cfg:tester:start_cmd.md),
[`start_env`](serve.cfg:tester:start_env.md),
[`time_limit_adjustment`](serve.cfg:tester:time_limit_adjustment.md).

При этом при наследовании конфигурационных переменных
[`check_cmd`](serve.cfg:tester:check_cmd.md),
[`check_dir`](serve.cfg:tester:check_dir.md),
[`errorcode_file`](serve.cfg:tester:errorcode_file.md),
[`error_file`](serve.cfg:tester:error_file.md),
[`prepare_cmd`](serve.cfg:tester:prepare_cmd.md),
[`run_dir`](serve.cfg:tester:run_dir.md),
[`start_cmd`](serve.cfg:tester:start_cmd.md) выполняется
[форматная подстановка](форматная_подстановка.md).

**Не наследуются** следующие конфигурационные переменные абстрактной
задачи: [`abstract`](serve.cfg:tester:abstract.md),
[`any`](serve.cfg:tester:any.md),
[`id`](serve.cfg:tester:id.md),
[`name`](serve.cfg:tester:name.md),
[`problem`](serve.cfg:tester:problem.md),
[`problem_name`](serve.cfg:tester:problem_name.md),
[`super`](serve.cfg:tester:super.md).

**Пример.**

`abstract`
