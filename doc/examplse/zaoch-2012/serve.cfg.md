Навигация: [Главная страница](../../main_Page.md)/[Система
ejudge](../../система_ejudge.md)/[Использование](../../использование.md)/[Примеры
конфигурационных
файлов](../../примеры_конфигурационных_файлов.md)/[Заочка-2012](serve.cfg.md)

`contest_id = 25`  
  
[`contest_time`](../../serve.cfg/global/contest_time.md)` = 0         # не ограниченный по времени турнир`  
[`score_system`](../../serve.cfg/global/score_system.md)` = kirov`  
[`board_fog_time`](../../serve.cfg/global/board_fog_time.md)` = 0       # без "заморозки" таблицы результатов`  
[`board_unfog_time`](../../serve.cfg/global/board_unfog_time.md)` = 0`  
[`standings_locale`](../../serve.cfg/global/standings_locale.md)` = "ru"  # таблица результатов на русском языке`  
  
`compile_dir = "../../compile/var/compile"`  
  
[`separate_user_score`](../../serve.cfg/global/separate_user_score.md)`      # хранить отдельные баллы для участников`  
[`team_enable_src_view`](../../serve.cfg/global/team_enable_src_view.md)`     # разрешить участникам просмотр их исходного кода`  
[`team_enable_rep_view`](../../serve.cfg/global/team_enable_rep_view.md)  
[`team_enable_ce_view`](../../serve.cfg/global/team_enable_ce_view.md)  
[`ignore_compile_errors`](../../serve.cfg/global/ignore_compile_errors.md)  
[`prune_empty_users`](../../serve.cfg/global/prune_empty_users.md)  
[`notify_clar_reply`](../../serve.cfg/global/notify_clar_reply.md)  
[`enable_eoln_select`](../../serve.cfg/global/enable_eoln_select.md)`       # разрешить участникам выбор типа концов строк`  
  
[`max_run_total`](../../serve.cfg/global/max_run_total.md)` = 10M`  
[`max_run_num`](../../serve.cfg/global/max_run_num.md)` = 500`  
  
[`team_info_url`](../../serve.cfg/global/team_info_url.md)` = "`[`http://olympiads.ru/cgi-bin/users?contest_id=25&user_id=%Mi&locale_id=1`](http://olympiads.ru/cgi-bin/users?contest_id=25&user_id=%Mi&locale_id=1)`"`  
[`standings_file_name`](../../serve.cfg/global/standings_file_name.md)` = "standings.shtml"`  
[`users_on_page`](../../serve.cfg/global/users_on_page.md)` = 100`  
[`stand_header_file`](../../serve.cfg/global/stand_header_file.md)` = "s_header.shtml"`  
[`stand_footer_file`](../../serve.cfg/global/stand_footer_file.md)` = "s_footer.shtml"`  
[`stand_symlink_dir`](../../serve.cfg/global/stand_symlink_dir.md)` = "olympiads.ru/html/zaoch/2012-13/standings/"`  
  
[`stand_show_att_num`](../../serve.cfg/global/stand_show_att_num.md)  
[`stand_extra_format`](../../serve.cfg/global/stand_extra_format.md)` = "<b>%Mr</b>: %Mc, %Mt, %UMp1c"`  
[`stand_extra_legend`](../../serve.cfg/global/stand_extra_legend.md)` = "Регион, город, школа, класс"`  
[`stand_extra_attr`](../../serve.cfg/global/stand_extra_attr.md)` = " width=\"120\" class=\"st_extra\""`  
  
[`rounding_mode`](../../serve.cfg/global/rounding_mode.md)` = floor`  
[`show_astr_time`](../../serve.cfg/global/show_astr_time.md)  
[`enable_runlog_merge`](../../serve.cfg/global/enable_runlog_merge.md)  
[`secure_run`](../../serve.cfg/global/secure_run.md)  
[`detect_violations`](../../serve.cfg/global/detect_violations.md)  
[`enable_memory_limit_error`](../../serve.cfg/global/enable_memory_limit_error.md)  
[`advanced_layout`](../../serve.cfg/global/advanced_layout.md)  
[`ignore_bom`](../../serve.cfg/global/ignore_bom.md)  
[`enable_l10n`](../../serve.cfg/global/enable_l10n.md)  
[`standings_charset`](../../serve.cfg/global/standings_charset.md)` = "koi8-r"`  
[`cpu_bogomips`](../../serve.cfg/global/cpu_bogomips.md)` = 5885`  
  
`[language]`  
[`id`](../../serve.cfg/language/id.md)` = 1`  
[`short_name`](../../serve.cfg/language/short_name.md)` = "fpc"`  
[`long_name`](../../serve.cfg/language/long_name.md)` = "Free Pascal 2.6.0"`  
[`src_sfx`](../../serve.cfg/language/src_sfx.md)` = ".pas"`  
  
`[language]`  
`id = 2`  
`short_name = "gcc"`  
`long_name = "GNU C 4.7.2"`  
`src_sfx = ".c"`  
  
`[language]`  
`id = 3`  
`short_name = "g++"`  
`long_name = "GNU C++ 4.7.2"`  
`src_sfx = ".cpp"`  
  
`[language]`  
`id = 6`  
`short_name = "gfortran"`  
`long_name = "GNU Fortran 4.7.2"`  
`src_sfx = ".for"`  
  
`[language]`  
`id = 8`  
`short_name = "dcc"`  
`long_name = "Borland Delphi 6 (Kylix) 14.5"`  
[`arch`](../../serve.cfg/language/arch.md)` = "linux-shared-32"`  
`src_sfx = ".pas"`  
  
`[language]`  
`id = 12`  
`short_name = "mzscheme"`  
`long_name = "MzScheme 4.1.2"`  
`arch = "linux-shared"`  
`src_sfx = ".scm"`  
  
`[language]`  
`id = 13`  
`short_name = "python"`  
`long_name = "Python 2.7"`  
`arch = "linux-shared"`  
`src_sfx = ".py"`  
  
`[language]`  
`id = 14`  
`short_name = "perl"`  
`long_name = "Perl 5.12.4"`  
`arch = "linux-shared"`  
`src_sfx = ".pl"`  
  
`[language]`  
`id = 15`  
`short_name = "gprolog"`  
`long_name = "GNU Prolog 1.3.1"`  
`arch = "linux-shared"`  
`src_sfx = ".pro"`  
  
`[language]`  
`id = 18`  
`short_name = "javac"`  
`long_name = "Java JDK 1.7.0_10"`  
`arch = "java"`  
`src_sfx = ".java"`  
`exe_sfx = ".jar"`  
  
`[language]`  
`id = 21`  
`short_name = "ruby"`  
`long_name = "Ruby 1.8.7"`  
`arch = "linux-shared"`  
`src_sfx = ".rb"`  
  
`[language]`  
`id = 22`  
`short_name = "php"`  
`long_name = "PHP 5.3.8"`  
`arch = "linux-shared"`  
`src_sfx = ".php"`  
  
`[language]`  
`id = 23`  
`short_name = "python3"`  
`long_name = "Python 3.1.2"`  
`arch = "linux-shared"`  
`src_sfx = ".py"`  
  
`[language]`  
`id = 26`  
`short_name = "ghc"`  
`long_name = "The Glasgow Haskell Compiler 7.4.2"`  
`arch = "linux-shared"`  
`src_sfx = ".hs"`  
  
`[language]`  
`id = 50`  
`short_name = "nasm-x86"`  
`long_name = "NASM 2.09.03"`  
`arch = "linux-shared-32"`  
`src_sfx = ".asm"`  
  
`[language]`  
`id = 51`  
`short_name = "clang"`  
`long_name = "clang C 3.2"`  
`arch = "linux-shared"`  
`src_sfx = ".c"`  
  
`[language]`  
`id = 52`  
`short_name = "clang++"`  
`long_name = "clang C++ 3.2"`  
`arch = "linux-shared"`  
`src_sfx = ".cpp"`  
  
`[problem]`  
[`abstract`](../../serve.cfg/problem/abstract.md)  
[`short_name`](../../serve.cfg/problem/short_name.md)` = "Generic"`  
[`use_stdin`](../../serve.cfg/problem/use_stdin.md)  
[`input_file`](../../serve.cfg/problem/input_file.md)` = "input.txt"`  
[`combined_stdin`](../../serve.cfg/problem/combined_stdin.md)  
[`use_stdout`](../../serve.cfg/problem/use_stdout.md)  
[`output_file`](../../serve.cfg/problem/output_file.md)` = "output.txt"`  
[`combined_stdout`](../../serve.cfg/problem/combined_stdout.md)  
[`score_latest`](../../serve.cfg/problem/score_latest.md)  
[`test_pat`](../../serve.cfg/problem/test_pat.md)` = "%02d"`  
[`use_corr`](../../serve.cfg/problem/use_corr.md)  
[`corr_pat`](../../serve.cfg/problem/corr_pat.md)` = "%02d.a"`  
[`time_limit`](../../serve.cfg/problem/time_limit.md)` = 1`  
[`real_time_limit`](../../serve.cfg/problem/real_time_limit.md)` = 5`  
[`max_vm_size`](../../serve.cfg/problem/max_vm_size.md)` = 256M`  
[`full_score`](../../serve.cfg/problem/full_score.md)` = 100`  
[`run_penalty`](../../serve.cfg/problem/run_penalty.md)` = 0`  
[`check_cmd`](../../serve.cfg/problem/check_cmd.md)` = "check"`  
[`interactive_valuer`](../../serve.cfg/problem/interactive_valuer.md)  
[`valuer_cmd`](../../serve.cfg/problem/valuer_cmd.md)` = "../gvaluer"`  
  
`[problem]`  
[`id`](../../serve.cfg/problem/id.md)` = 1`  
[`super`](../../serve.cfg/problem/super.md)` = "Generic"`  
[`short_name`](../../serve.cfg/problem/short_name.md)` = "A"`  
[`long_name`](../../serve.cfg/problem/long_name.md)` = "Канарейки"`  
[`internal_name`](../../serve.cfg/problem/internal_name.md)` = "rabbits"`  
[`extid`](../../serve.cfg/problem/extid.md)` = "polygon:rabbits"`  
[`max_vm_size`](../../serve.cfg/problem/max_vm_size.md)` = 256M`  
[`max_stack_size`](../../serve.cfg/problem/max_stack_size.md)` = 128M`  
[`full_user_score`](../../serve.cfg/problem/full_user_score.md)` = 100`  
[`standard_checker`](../../serve.cfg/problem/standard_checker.md)` = "cmp_long_long_seq"`  
[`solution_cmd`](../../serve.cfg/problem/solution_cmd.md)` = "zoo_ap"`  
  
`[problem]`  
`id = 2`  
`super = "Generic"`  
`short_name = "B"`  
`long_name = "Страусиная ферма"`  
`internal_name = "ostriches"`  
`extid = "polygon:ostriches"`  
`max_vm_size = 256M`  
`max_stack_size = 64M`  
`full_user_score = 100`  
[`open_tests`](../../serve.cfg/problem/open_tests.md)` = "1-35:brief, 36-55:brief"`  
[`final_open_tests`](../../serve.cfg/problem/final_open_tests.md)` = "1-55"`  
`solution_cmd = "clev"`  
  
`[problem]`  
`id = 3`  
`super = "Generic"`  
`short_name = "C"`  
`long_name = "Кафельная плитка"`  
`internal_name = "tiles"`  
`extid = "polygon:tiles"`  
`max_vm_size = 256M`  
`max_stack_size = 64M`  
`full_user_score = 100`  
`standard_checker = "cmp_huge_int"`  
`solution_cmd = "tiles_ha"`  
  
`[problem]`  
`id = 4`  
`super = "Generic"`  
`short_name = "D"`  
`long_name = "Нумерация серий"`  
`internal_name = "futurama"`  
`extid = "polygon:futurama"`  
`max_vm_size = 256M`  
`max_stack_size = 256M`  
`full_user_score = 100`  
`standard_checker = "cmp_file_nospace"`  
`solution_cmd = "futurama_at"`  
  
`[problem]`  
`id = 5`  
`super = "Generic"`  
`short_name = "E"`  
`long_name = "Распродажа"`  
`internal_name = "knapsack"`  
`extid = "polygon:knapsack"`  
`time_limit = 3`  
`real_time_limit = 6`  
`max_vm_size = 256M`  
`max_stack_size = 256M`  
`full_user_score = 60`  
`open_tests = "1:full, 2-7:brief, 8-11:brief, 12-23:hidden"`  
`solution_cmd = "knapsack_poland"`  
  
`[problem]`  
`id = 6`  
`super = "Generic"`  
`short_name = "F"`  
`long_name = "Числа в Зазеркалье"`  
`internal_name = "mirror"`  
`extid = "polygon:mirror"`  
`time_limit = 2`  
`max_vm_size = 256M`  
`max_stack_size = 256M`  
`full_user_score = 60`  
`open_tests = "1-2: full, 3-26:brief, 27-32:brief, 33-40:hidden"`  
`final_open_tests = "1-40"`  
`standard_checker = "cmp_huge_int"`  
`solution_cmd = "mirror_ap"`  
  
`[problem]`  
`id = 7`  
`super = "Generic"`  
`short_name = "G"`  
`long_name = "Правила дорожного движения"`  
`internal_name = "forbidden"`  
`extid = "polygon:forbidden"`  
`time_limit = 3`  
`max_vm_size = 256M`  
`max_stack_size = 256M`  
`full_user_score = 60`  
`open_tests = "1: full, 2-10:brief, 11-20:brief, 21-47:hidden"`  
`final_open_tests = "1-40"`  
`standard_checker = "cmp_long_long_seq"`  
`solution_cmd = "forbidden_at_bfs_fast_scanf"`  
  
`[problem]`  
`id = 8`  
`super = "Generic"`  
`short_name = "H"`  
`long_name = "Петя отдыхает"`  
`internal_name = "holidays"`  
`extid = "polygon:holidays"`  
`time_limit = 1`  
`max_vm_size = 256M`  
`max_stack_size = 256M`  
`full_user_score = 40`  
`open_tests = "1-2: full, 3-9:brief, 10-18:brief, 19-33:hidden"`  
`standard_checker = "cmp_long_long_seq"`  
`solution_cmd = "sol"`  
  
`[problem]`  
`id = 9`  
`super = "Generic"`  
`short_name = "I"`  
`long_name = "Расшифровка"`  
`internal_name = "similarity"`  
`extid = "polygon:similarity"`  
`time_limit = 1`  
`max_vm_size = 256M`  
`max_stack_size = 256M`  
`full_user_score = 60`  
`open_tests = "1-3: full, 4-15:brief, 16-40:brief, 41-75:brief, 76-115:hidden"`  
`check_cmd = "checker"`  
`solution_cmd = "sol_lopatin"`  
  
`[problem]`  
`id = 10`  
`super = "Generic"`  
`short_name = "J"`  
`long_name = "Страусиные страсти"`  
`internal_name = "trinagulations"`  
`extid = "polygon:trinagulations"`  
`time_limit = 1`  
`max_vm_size = 256M`  
`max_stack_size = 256M`  
`full_user_score = 40`  
`open_tests = "1-2: full, 3-18:brief, 19-26:brief, 27-42:hidden"`  
`check_cmd = "checker"`  
`solution_cmd = "stup"`  
  
`[problem]`  
`id = 11`  
`super = "Generic"`  
`short_name = "K"`  
`long_name = "Стулья"`  
`internal_name = "chairs"`  
`extid = "polygon:chairs"`  
`time_limit = 2`  
`max_vm_size = 256M`  
`max_stack_size = 256M`  
`full_user_score = 30`  
`open_tests = "1-2: full, 3-20:brief, 21-50:hidden"`  
`solution_cmd = "chairs_at"`  
  
`[problem]`  
`id = 12`  
`super = "Generic"`  
`short_name = "L"`  
`long_name = "Phigon"`  
`internal_name = "python"`  
`extid = "polygon:python"`  
`time_limit = 3`  
`real_time_limit = 6`  
`max_vm_size = 256M`  
`max_stack_size = 256M`  
`full_user_score = 60`  
`open_tests = "1-3: full, 4-26:brief, 27-39:brief, 40-50:hidden"`  
`solution_cmd = "python_mp_DIECONTESTANT"`  
  
`[problem]`  
`id = 13`  
`super = "Generic"`  
`short_name = "M"`  
`long_name = "Охота на короля"`  
`internal_name = "chess2"`  
`time_limit = 3`  
`real_time_limit = 6`  
`max_vm_size = 256M`  
`max_stack_size = 256M`  
`full_user_score = 40`  
`open_tests = "1-13: full, 14-26:full, 27-39:hidden, 40-52:hidden, 53-65:hidden"`  
[`interactor_cmd`](../../serve.cfg/problem/interactor_cmd.md)` = "interactor"`  
[`interactor_time_limit`](../../serve.cfg/problem/interactor_time_limit.md)` = 10`  
`solution_cmd = "check"`  
`team_enable_rep_view`
