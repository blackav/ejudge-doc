Навигация: [Главная страница](../../main_Page.md)/[Система
ejudge](../../система_ejudge.md)/[Использование](../../использование.md)/[Конфигурационные
файлы](../../конфигурационные_файлы.md)/[serve.cfg](../../serve.cfg.md)/[Конфигурационные
параметры
задач](../problem.md)/[abstract](abstract.md)

|                            |                                           |
|----------------------------|-------------------------------------------|
| **Имя переменной**:        | **`abstract`**                            |
| **Содержится в:**          | [`problem`](../problem.md) |
| **Используется:**          | `serve, run`                              |
| **Тип содержимого:**       | *boolean*                                 |
| **Может отсутствовать:**   | *да*                                      |
| **Значение по умолчанию:** | *false*                                   |
| **Может повторяться:**     | *нет*                                     |

**Описание.** Если данная конфигурационная переменная установлена в
*true*, текущее описание задачи является описанием абстрактной задачи.
Абстрактная задача не может иметь идентификатора задачи
([`id`](id.md)) или длинного имени задачи
([`long_name`](long_name.md)), но должна иметь
короткое имя ([`short_name`](short_name.md)),
уникальное среди всех абстрактных задач. Абстрактная задаче не может
наследовать свойства другой абстрактной задачи, то есть в абстрактных
задачах запрещено использование конфигурационной переменной
[`super`](super.md). Значения конфигурационных
переменных, установленные в некоторой абстрактной задаче, наследуются
конкретной задачей, указавшей данную абстрактную задачу в значении своей
конфигурационной переменной `super`.

Конкретная задача наследует следующие конфигурационные переменные из
описания абстрактной задачи:
[`accept_partial`](accept_partial.md),
[`checker_real_time_limit`](checker_real_time_limit.md),
[`corr_dir`](corr_dir.md),
[`corr_sfx`](corr_sfx.md),
[`disable_auto_testing`](disable_auto_testing.md),
[`disable_testing`](disable_testing.md),
[`full_score`](full_score.md),
[`hidden`](hidden.md),
[`info_dir`](info_dir.md),
[`info_sfx`](info_sfx.md),
[`input_file`](input_file.md),
[`output_file`](output_file.md),
[`real_time_limit`](real_time_limit.md),
[`run_penalty`](run_penalty.md),
[`team_enable_ce_view`](team_enable_ce_view.md),
[`team_enable_rep_view`](team_enable_rep_view.md),
[`team_show_judge_report`](team_show_judge_report.md),
[`test_dir`](test_dir.md),
[`test_score`](test_score.md),
[`test_sfx`](test_sfx.md),
[`test_to_accept`](serve.cfg:problem:test_to_accept.md),
[`tgz_dir`](tgz_dir.md),
[`tgz_sfx`](tgz_sfx.md),
[`time_limit`](time_limit.md),
[`use_corr`](use_corr.md),
[`use_info`](use_info.md),
[`use_stdin`](use_stdin.md),
[`use_stdout`](use_stdout.md),
[`use_tgz`](use_tgz.md),
[`variable_full_score`](variable_full_score.md),
[`variant_num`](variant_num.md).

При этом при наследовании конфигурационных переменных
[`corr_dir`](corr_dir.md),
[`info_dir`](info_dir.md),
[`input_file`](input_file.md),
[`output_file`](output_file.md),
[`test_dir_tgz_dir`](serve.cfg:problem:test_dir_tgz_dir.md)
выполняется [форматная подстановка](форматная_подстановка.md).

**Не наследуются** следующие конфигурационные переменные абстрактной
задачи: [`abstract`](abstract.md),
[`deadline`](deadline.md),
[`id`](id.md),
[`long_name`](long_name.md),
[`short_name`](short_name.md),
[`super`](super.md),
[`tester_id`](tester_id.md),[`test_score_list`](test_score_list.md),
[`test_sets`](test_sets.md).
