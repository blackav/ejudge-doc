Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[contest.xml](contest.xml "wikilink")

В данном разделе даётся описание формата файла описания параметров
турнира. [Подробнее...](contest.xml:info "wikilink")

- [Регистрационная анкета
  пользователя](Регистрационная_анкета_пользователя "wikilink")

Конфигурационные файлы описания базовых настроек турнира (XML-файлы
турнира) находятся в каталоге EJUDGE_CONTESTS_HOME_DIR/data/contests.
Имя файла — это номер турнира дополненный до 6 цифр слева нулями.
Например, для турнира 1 файл его конфигурации называется 000001.xml.
Если при конфигуриривании ejudge параметр EJUDGE_CONTESTS_HOME_DIR
установлен в /home/judges, то полный путь к XML-файлу конфигурации
турнира 1 будет равен /home/judges/data/contests/000001.xml.

Конфигурационные файлы базовых настроек турнира автоматически
перечитываются системой ejudge при их обновлении. То есть, если в файл
было внесено изменение (либо вручную с помощью текстового редактора,
либо с помощью веб-интерфейса редактирования настроек турнира), новая
версия файла будет автоматически загружена в систему.

### Элементы файла

- [`advisors`](contest.xml:contestants_reserves_coaches_advisors_guests "wikilink")
- [`allowed_languages`](contest.xml:allowed_languages "wikilink")
- [`allowed_regions`](contest.xml:allowed_regions "wikilink")
- [`avatar_plugin`](contest.xml:avatar_plugin "wikilink")
- [`cap`](contest.xml:cap "wikilink")
- [`caps`](contest.xml:caps "wikilink")
- [`cf_notify_email`](contest.xml:cf_notify_email "wikilink")
- [`clar_notify_email`](contest.xml:clar_notify_email "wikilink")
- [`client_flags`](contest.xml:client_flags "wikilink")
- [`close_time`](contest.xml:close_time "wikilink")
- [`comment`](contest.xml:comment "wikilink")
- [`content_plugin`](contest.xml:content_plugin "wikilink")
- [`content_url_prefix`](contest.xml:content_url_prefix "wikilink")
- [`coaches`](contest.xml:contestants_reserves_coaches_advisors_guests "wikilink")
- [`conf_dir`](contest.xml:conf_dir "wikilink")
- [`contest`](contest.xml:contest "wikilink")
- [`contestants`](contest.xml:contestants_reserves_coaches_advisors_guests "wikilink")
- [`copyright_file`](contest.xml:copyright_file "wikilink")
- [`css_url`](contest.xml:css_url "wikilink")
- [`daily_stat_email`](contest.xml:daily_stat_email "wikilink")
- [`default_locale`](contest.xml:default_locale "wikilink")
- [`dir_group`](contest.xml:dir_group "wikilink")
- [`dir_mode`](contest.xml:dir_mode "wikilink")
- [`ext_id`](contest.xml:ext_id "wikilink")
- [`field`](contest.xml:field "wikilink")
- [`file_group`](contest.xml:file_group "wikilink")
- [`file_mode`](contest.xml:file_mode "wikilink")
- [`guests`](contest.xml:contestants_reserves_coaches_advisors_guests "wikilink")
- [`ip`](contest.xml:ip "wikilink")
- [`judge_access`](contest.xml:judge_access "wikilink")
- [`keywords`](contest.xml:keywords "wikilink")
- [`login_template`](contest.xml:login_template "wikilink")
- [`login_template_options`](contest.xml:login_template_options "wikilink")
- [`logo_url`](contest.xml:logo_url "wikilink")
- [`main_url`](contest.xml:main_url "wikilink")
- [`master_access`](contest.xml:master_access "wikilink")
- [`name`](contest.xml:name "wikilink")
- [`name_en`](contest.xml:name_en "wikilink")
- [`oauth_rule`](contest.xml:oauth_rule "wikilink")
- [`oauth_rules`](contest.xml:oauth_rules "wikilink")
- [`open_time`](contest.xml:open_time "wikilink")
- [`priv_footer_file`](contest.xml:priv_footer_file "wikilink")
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0 "wikilink")</i>)
- [`priv_header_file`](contest.xml:priv_header_file "wikilink")
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0 "wikilink")</i>)
- [`problem_count`](contest.xml:problem_count "wikilink")
- [`problems_url`](contest.xml:problems_url "wikilink")
- [`sched_time`](contest.xml:sched_time "wikilink")
- [`serve_control_access`](contest.xml:serve_control_access "wikilink")
- [`serve_group`](contest.xml:serve_group "wikilink")
- [`serve_user`](contest.xml:serve_user "wikilink")
- [`slave_rules`](contest.xml:slave_rules "wikilink")
- [`special_flow_options`](contest.xml:special_flow_options "wikilink")
- [`standings_url`](contest.xml:standings_url "wikilink")
- [`register_access`](contest.xml:register_access "wikilink")
- [`register_email`](contest.xml:register_email "wikilink")
- [`register_email_file`](contest.xml:register_email_file "wikilink")
- [`register_footer_file`](contest.xml:register_footer_file "wikilink")
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0 "wikilink")</i>)
- [`register_header_file`](contest.xml:register_header_file "wikilink")
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0 "wikilink")</i>)
- [`register_head_style`](contest.xml:register_head_style "wikilink")
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0 "wikilink")</i>)
- [`register_par_style`](contest.xml:register_par_style "wikilink")
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0 "wikilink")</i>)
- [`register_subject`](contest.xml:register_subject "wikilink")
- [`register_subject_en`](contest.xml:register_subject_en "wikilink")
- [`register_table_style`](contest.xml:register_table_style "wikilink")
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0 "wikilink")</i>)
- [`register_url`](contest.xml:register_url "wikilink")
- [`registration_deadline`](contest.xml:registration_deadline "wikilink")
- [`reg_welcome_file`](contest.xml:reg_welcome_file "wikilink")
- [`reserves`](contest.xml:reserves "wikilink")
- [`root_dir`](contest.xml:root_dir "wikilink")
- [`run_group`](contest.xml:run_group "wikilink")
- [`run_managed_on`](contest.xml:run_managed_on "wikilink")
- [`run_user`](contest.xml:run_user "wikilink")
- [`team_access`](contest.xml:team_access "wikilink")
- [`team_footer_file`](contest.xml:team_footer_file "wikilink")
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0 "wikilink")</i>)
- [`team_header_file`](contest.xml:team_header_file "wikilink")
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0 "wikilink")</i>)
- [`team_head_style`](contest.xml:team_head_style "wikilink")
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0 "wikilink")</i>)
- [`team_menu_1_file`](contest.xml:team_menu_1_file "wikilink")
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0 "wikilink")</i>)
- [`team_menu_2_file`](contest.xml:team_menu_2_file "wikilink")
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0 "wikilink")</i>)
- [`team_menu_3_file`](contest.xml:team_menu_3_file "wikilink")
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0 "wikilink")</i>)
- [`team_par_style`](contest.xml:team_par_style "wikilink")
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0 "wikilink")</i>)
- [`team_separator_file`](contest.xml:team_separator_file "wikilink")
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0 "wikilink")</i>)
- [`team_url`](contest.xml:team_url "wikilink")
- [`telegram_admin_chat_id`](contest.xml:telegram_admin_chat_id "wikilink")
- [`telegram_bot_id`](contest.xml:telegram_bot_id "wikilink")
- [`telegram_user_chat_id`](contest.xml:telegram_user_chat_id "wikilink")
- [`update_time`](contest.xml:update_time "wikilink")
- [`user_contest`](contest.xml:user_contest "wikilink")
- [`user_name_comment`](contest.xml:user_name_comment "wikilink")
- [`users_access`](contest.xml:users_access "wikilink")
- [`users_footer_file`](contest.xml:users_footer_file "wikilink")
- [`users_header_file`](contest.xml:users_header_file "wikilink")
- [`users_head_style`](contest.xml:users_head_style "wikilink")
- [`users_par_style`](contest.xml:users_par_style "wikilink")
- [`users_table_format`](contest.xml:users_table_format "wikilink")
- [`users_table_format_en`](contest.xml:users_table_format_en "wikilink")
- [`users_table_legend`](contest.xml:users_table_legend "wikilink")
- [`users_table_legend_en`](contest.xml:users_table_legend_en "wikilink")
- [`users_table_style`](contest.xml:users_table_style "wikilink")
- [`users_verb_style`](contest.xml:users_verb_style "wikilink")
- [`welcome_file`](contest.xml:welcome_file "wikilink")
