Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[abstract](serve.cfg:problem:abstract "wikilink")

|                            |                                           |
|----------------------------|-------------------------------------------|
| **Имя переменной**:        | **`abstract`**                            |
| **Содержится в:**          | [`problem`](serve.cfg:problem "wikilink") |
| **Используется:**          | `serve, run`                              |
| **Тип содержимого:**       | *boolean*                                 |
| **Может отсутствовать:**   | *да*                                      |
| **Значение по умолчанию:** | *false*                                   |
| **Может повторяться:**     | *нет*                                     |

**Описание.** Если данная конфигурационная переменная установлена в
*true*, текущее описание задачи является описанием абстрактной задачи.
Абстрактная задача не может иметь идентификатора задачи
([`id`](serve.cfg:problem:id "wikilink")) или длинного имени задачи
([`long_name`](serve.cfg:problem:long_name "wikilink")), но должна иметь
короткое имя ([`short_name`](serve.cfg:problem:short_name "wikilink")),
уникальное среди всех абстрактных задач. Абстрактная задаче не может
наследовать свойства другой абстрактной задачи, то есть в абстрактных
задачах запрещено использование конфигурационной переменной
[`super`](serve.cfg:problem:super "wikilink"). Значения конфигурационных
переменных, установленные в некоторой абстрактной задаче, наследуются
конкретной задачей, указавшей данную абстрактную задачу в значении своей
конфигурационной переменной `super`.

Конкретная задача наследует следующие конфигурационные переменные из
описания абстрактной задачи:
[`accept_partial`](serve.cfg:problem:accept_partial "wikilink"),
[`checker_real_time_limit`](serve.cfg:problem:checker_real_time_limit "wikilink"),
[`corr_dir`](serve.cfg:problem:corr_dir "wikilink"),
[`corr_sfx`](serve.cfg:problem:corr_sfx "wikilink"),
[`disable_auto_testing`](serve.cfg:problem:disable_auto_testing "wikilink"),
[`disable_testing`](serve.cfg:problem:disable_testing "wikilink"),
[`full_score`](serve.cfg:problem:full_score "wikilink"),
[`hidden`](serve.cfg:problem:hidden "wikilink"),
[`info_dir`](serve.cfg:problem:info_dir "wikilink"),
[`info_sfx`](serve.cfg:problem:info_sfx "wikilink"),
[`input_file`](serve.cfg:problem:input_file "wikilink"),
[`output_file`](serve.cfg:problem:output_file "wikilink"),
[`real_time_limit`](serve.cfg:problem:real_time_limit "wikilink"),
[`run_penalty`](serve.cfg:problem:run_penalty "wikilink"),
[`team_enable_ce_view`](serve.cfg:problem:team_enable_ce_view "wikilink"),
[`team_enable_rep_view`](serve.cfg:problem:team_enable_rep_view "wikilink"),
[`team_show_judge_report`](serve.cfg:problem:team_show_judge_report "wikilink"),
[`test_dir`](serve.cfg:problem:test_dir "wikilink"),
[`test_score`](serve.cfg:problem:test_score "wikilink"),
[`test_sfx`](serve.cfg:problem:test_sfx "wikilink"),
[`test_to_accept`](serve.cfg:problem:test_to_accept "wikilink"),
[`tgz_dir`](serve.cfg:problem:tgz_dir "wikilink"),
[`tgz_sfx`](serve.cfg:problem:tgz_sfx "wikilink"),
[`time_limit`](serve.cfg:problem:time_limit "wikilink"),
[`use_corr`](serve.cfg:problem:use_corr "wikilink"),
[`use_info`](serve.cfg:problem:use_info "wikilink"),
[`use_stdin`](serve.cfg:problem:use_stdin "wikilink"),
[`use_stdout`](serve.cfg:problem:use_stdout "wikilink"),
[`use_tgz`](serve.cfg:problem:use_tgz "wikilink"),
[`variable_full_score`](serve.cfg:problem:variable_full_score "wikilink"),
[`variant_num`](serve.cfg:problem:variant_num "wikilink").

При этом при наследовании конфигурационных переменных
[`corr_dir`](serve.cfg:problem:corr_dir "wikilink"),
[`info_dir`](serve.cfg:problem:info_dir "wikilink"),
[`input_file`](serve.cfg:problem:input_file "wikilink"),
[`output_file`](serve.cfg:problem:output_file "wikilink"),
[`test_dir_tgz_dir`](serve.cfg:problem:test_dir_tgz_dir "wikilink")
выполняется [форматная подстановка](форматная_подстановка "wikilink").

**Не наследуются** следующие конфигурационные переменные абстрактной
задачи: [`abstract`](serve.cfg:problem:abstract "wikilink"),
[`deadline`](serve.cfg:problem:deadline "wikilink"),
[`id`](serve.cfg:problem:id "wikilink"),
[`long_name`](serve.cfg:problem:long_name "wikilink"),
[`short_name`](serve.cfg:problem:short_name "wikilink"),
[`super`](serve.cfg:problem:super "wikilink"),
[`tester_id`](serve.cfg:problem:tester_id "wikilink"),[`test_score_list`](serve.cfg:problem:test_score_list "wikilink"),
[`test_sets`](serve.cfg:problem:test_sets "wikilink").
