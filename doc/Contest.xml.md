Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[contest.xml](contest.xml.md)

В данном разделе даётся описание формата файла описания параметров
турнира. [Подробнее...](contest.xml:info.md)

- [Регистрационная анкета
  пользователя](Регистрационная_анкета_пользователя.md)

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

- [`advisors`](contest.xml:contestants_reserves_coaches_advisors_guests.md)
- [`allowed_languages`](contest.xml:allowed_languages.md)
- [`allowed_regions`](contest.xml:allowed_regions.md)
- [`avatar_plugin`](contest.xml:avatar_plugin.md)
- [`cap`](contest.xml:cap.md)
- [`caps`](contest.xml:caps.md)
- [`cf_notify_email`](contest.xml:cf_notify_email.md)
- [`clar_notify_email`](contest.xml:clar_notify_email.md)
- [`client_flags`](contest.xml:client_flags.md)
- [`close_time`](contest.xml:close_time.md)
- [`comment`](contest.xml:comment.md)
- [`content_plugin`](contest.xml:content_plugin.md)
- [`content_url_prefix`](contest.xml:content_url_prefix.md)
- [`coaches`](contest.xml:contestants_reserves_coaches_advisors_guests.md)
- [`conf_dir`](contest.xml:conf_dir.md)
- [`contest`](contest.xml:contest.md)
- [`contestants`](contest.xml:contestants_reserves_coaches_advisors_guests.md)
- [`copyright_file`](contest.xml:copyright_file.md)
- [`css_url`](contest.xml:css_url.md)
- [`daily_stat_email`](contest.xml:daily_stat_email.md)
- [`default_locale`](contest.xml:default_locale.md)
- [`dir_group`](contest.xml:dir_group.md)
- [`dir_mode`](contest.xml:dir_mode.md)
- [`ext_id`](contest.xml:ext_id.md)
- [`field`](contest.xml:field.md)
- [`file_group`](contest.xml:file_group.md)
- [`file_mode`](contest.xml:file_mode.md)
- [`guests`](contest.xml:contestants_reserves_coaches_advisors_guests.md)
- [`ip`](contest.xml:ip.md)
- [`judge_access`](contest.xml:judge_access.md)
- [`keywords`](contest.xml:keywords.md)
- [`login_template`](contest.xml:login_template.md)
- [`login_template_options`](contest.xml:login_template_options.md)
- [`logo_url`](contest.xml:logo_url.md)
- [`main_url`](contest.xml:main_url.md)
- [`master_access`](contest.xml:master_access.md)
- [`name`](contest.xml:name.md)
- [`name_en`](contest.xml:name_en.md)
- [`oauth_rule`](contest.xml:oauth_rule.md)
- [`oauth_rules`](contest.xml:oauth_rules.md)
- [`open_time`](contest.xml:open_time.md)
- [`priv_footer_file`](contest.xml:priv_footer_file.md)
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0.md)</i>)
- [`priv_header_file`](contest.xml:priv_header_file.md)
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0.md)</i>)
- [`problem_count`](contest.xml:problem_count.md)
- [`problems_url`](contest.xml:problems_url.md)
- [`sched_time`](contest.xml:sched_time.md)
- [`serve_control_access`](contest.xml:serve_control_access.md)
- [`serve_group`](contest.xml:serve_group.md)
- [`serve_user`](contest.xml:serve_user.md)
- [`slave_rules`](contest.xml:slave_rules.md)
- [`special_flow_options`](contest.xml:special_flow_options.md)
- [`standings_url`](contest.xml:standings_url.md)
- [`register_access`](contest.xml:register_access.md)
- [`register_email`](contest.xml:register_email.md)
- [`register_email_file`](contest.xml:register_email_file.md)
- [`register_footer_file`](contest.xml:register_footer_file.md)
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0.md)</i>)
- [`register_header_file`](contest.xml:register_header_file.md)
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0.md)</i>)
- [`register_head_style`](contest.xml:register_head_style.md)
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0.md)</i>)
- [`register_par_style`](contest.xml:register_par_style.md)
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0.md)</i>)
- [`register_subject`](contest.xml:register_subject.md)
- [`register_subject_en`](contest.xml:register_subject_en.md)
- [`register_table_style`](contest.xml:register_table_style.md)
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0.md)</i>)
- [`register_url`](contest.xml:register_url.md)
- [`registration_deadline`](contest.xml:registration_deadline.md)
- [`reg_welcome_file`](contest.xml:reg_welcome_file.md)
- [`reserves`](contest.xml:reserves.md)
- [`root_dir`](contest.xml:root_dir.md)
- [`run_group`](contest.xml:run_group.md)
- [`run_managed_on`](contest.xml:run_managed_on.md)
- [`run_user`](contest.xml:run_user.md)
- [`team_access`](contest.xml:team_access.md)
- [`team_footer_file`](contest.xml:team_footer_file.md)
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0.md)</i>)
- [`team_header_file`](contest.xml:team_header_file.md)
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0.md)</i>)
- [`team_head_style`](contest.xml:team_head_style.md)
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0.md)</i>)
- [`team_menu_1_file`](contest.xml:team_menu_1_file.md)
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0.md)</i>)
- [`team_menu_2_file`](contest.xml:team_menu_2_file.md)
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0.md)</i>)
- [`team_menu_3_file`](contest.xml:team_menu_3_file.md)
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0.md)</i>)
- [`team_par_style`](contest.xml:team_par_style.md)
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0.md)</i>)
- [`team_separator_file`](contest.xml:team_separator_file.md)
  (<i>Игнорируется начиная с [версии
  3.0](Изменения_в_версии_3.0.md)</i>)
- [`team_url`](contest.xml:team_url.md)
- [`telegram_admin_chat_id`](contest.xml:telegram_admin_chat_id.md)
- [`telegram_bot_id`](contest.xml:telegram_bot_id.md)
- [`telegram_user_chat_id`](contest.xml:telegram_user_chat_id.md)
- [`update_time`](contest.xml:update_time.md)
- [`user_contest`](contest.xml:user_contest.md)
- [`user_name_comment`](contest.xml:user_name_comment.md)
- [`users_access`](contest.xml:users_access.md)
- [`users_footer_file`](contest.xml:users_footer_file.md)
- [`users_header_file`](contest.xml:users_header_file.md)
- [`users_head_style`](contest.xml:users_head_style.md)
- [`users_par_style`](contest.xml:users_par_style.md)
- [`users_table_format`](contest.xml:users_table_format.md)
- [`users_table_format_en`](contest.xml:users_table_format_en.md)
- [`users_table_legend`](contest.xml:users_table_legend.md)
- [`users_table_legend_en`](contest.xml:users_table_legend_en.md)
- [`users_table_style`](contest.xml:users_table_style.md)
- [`users_verb_style`](contest.xml:users_verb_style.md)
- [`welcome_file`](contest.xml:welcome_file.md)
