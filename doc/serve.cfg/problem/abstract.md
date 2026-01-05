Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Конфигурационные
параметры
задач](serve.cfg:problem.md)/[abstract](serve.cfg:problem:abstract.md)

|                            |                                           |
|----------------------------|-------------------------------------------|
| **Имя переменной**:        | **`abstract`**                            |
| **Содержится в:**          | [`problem`](serve.cfg:problem.md) |
| **Используется:**          | `serve, run`                              |
| **Тип содержимого:**       | *boolean*                                 |
| **Может отсутствовать:**   | *да*                                      |
| **Значение по умолчанию:** | *false*                                   |
| **Может повторяться:**     | *нет*                                     |

**Описание.** Если данная конфигурационная переменная установлена в
*true*, текущее описание задачи является описанием абстрактной задачи.
Абстрактная задача не может иметь идентификатора задачи
([`id`](serve.cfg:problem:id.md)) или длинного имени задачи
([`long_name`](serve.cfg:problem:long_name.md)), но должна иметь
короткое имя ([`short_name`](serve.cfg:problem:short_name.md)),
уникальное среди всех абстрактных задач. Абстрактная задаче не может
наследовать свойства другой абстрактной задачи, то есть в абстрактных
задачах запрещено использование конфигурационной переменной
[`super`](serve.cfg:problem:super.md). Значения конфигурационных
переменных, установленные в некоторой абстрактной задаче, наследуются
конкретной задачей, указавшей данную абстрактную задачу в значении своей
конфигурационной переменной `super`.

Конкретная задача наследует следующие конфигурационные переменные из
описания абстрактной задачи:
[`accept_partial`](serve.cfg:problem:accept_partial.md),
[`checker_real_time_limit`](serve.cfg:problem:checker_real_time_limit.md),
[`corr_dir`](serve.cfg:problem:corr_dir.md),
[`corr_sfx`](serve.cfg:problem:corr_sfx.md),
[`disable_auto_testing`](serve.cfg:problem:disable_auto_testing.md),
[`disable_testing`](serve.cfg:problem:disable_testing.md),
[`full_score`](serve.cfg:problem:full_score.md),
[`hidden`](serve.cfg:problem:hidden.md),
[`info_dir`](serve.cfg:problem:info_dir.md),
[`info_sfx`](serve.cfg:problem:info_sfx.md),
[`input_file`](serve.cfg:problem:input_file.md),
[`output_file`](serve.cfg:problem:output_file.md),
[`real_time_limit`](serve.cfg:problem:real_time_limit.md),
[`run_penalty`](serve.cfg:problem:run_penalty.md),
[`team_enable_ce_view`](serve.cfg:problem:team_enable_ce_view.md),
[`team_enable_rep_view`](serve.cfg:problem:team_enable_rep_view.md),
[`team_show_judge_report`](serve.cfg:problem:team_show_judge_report.md),
[`test_dir`](serve.cfg:problem:test_dir.md),
[`test_score`](serve.cfg:problem:test_score.md),
[`test_sfx`](serve.cfg:problem:test_sfx.md),
[`test_to_accept`](serve.cfg:problem:test_to_accept.md),
[`tgz_dir`](serve.cfg:problem:tgz_dir.md),
[`tgz_sfx`](serve.cfg:problem:tgz_sfx.md),
[`time_limit`](serve.cfg:problem:time_limit.md),
[`use_corr`](serve.cfg:problem:use_corr.md),
[`use_info`](serve.cfg:problem:use_info.md),
[`use_stdin`](serve.cfg:problem:use_stdin.md),
[`use_stdout`](serve.cfg:problem:use_stdout.md),
[`use_tgz`](serve.cfg:problem:use_tgz.md),
[`variable_full_score`](serve.cfg:problem:variable_full_score.md),
[`variant_num`](serve.cfg:problem:variant_num.md).

При этом при наследовании конфигурационных переменных
[`corr_dir`](serve.cfg:problem:corr_dir.md),
[`info_dir`](serve.cfg:problem:info_dir.md),
[`input_file`](serve.cfg:problem:input_file.md),
[`output_file`](serve.cfg:problem:output_file.md),
[`test_dir_tgz_dir`](serve.cfg:problem:test_dir_tgz_dir.md)
выполняется [форматная подстановка](форматная_подстановка.md).

**Не наследуются** следующие конфигурационные переменные абстрактной
задачи: [`abstract`](serve.cfg:problem:abstract.md),
[`deadline`](serve.cfg:problem:deadline.md),
[`id`](serve.cfg:problem:id.md),
[`long_name`](serve.cfg:problem:long_name.md),
[`short_name`](serve.cfg:problem:short_name.md),
[`super`](serve.cfg:problem:super.md),
[`tester_id`](serve.cfg:problem:tester_id.md),[`test_score_list`](serve.cfg:problem:test_score_list.md),
[`test_sets`](serve.cfg:problem:test_sets.md).
