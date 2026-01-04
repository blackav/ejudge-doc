Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[ejudge.xml](ejudge.xml "wikilink")

Этот конфигурационный файл содержит общие настройки системы ejudge,
которые используются всеми компонентами. Обычно этот файл находится по
пути `/home/judges/data/ejudge.xml`, то есть в подкаталоге `data`
каталога турниров.

### Общая структура

Конфигурационный файл должен быть корректным XML-файлом. Он должен
состоять из единственного элемента первого уровня config. Иерархия
элементов приведена на схеме ниже.

  
[`config`](ejudge.xml:config "wikilink")

  
[`caps`](ejudge.xml:caps "wikilink")

  
[`cap`](ejudge.xml:cap "wikilink")

[`caps_file`](ejudge.xml:caps_file "wikilink")

[`charset`](ejudge.xml:charset "wikilink") (\*)

[`compile_home_dir`](ejudge.xml:compile_home_dir "wikilink") (\*\*)

[`compile_log`](ejudge.xml:compile_log "wikilink") (\*\*)

[`compiler_options`](ejudge.xml:compiler_options "wikilink")

  
[`compiler_option`](ejudge.xml:compiler_option "wikilink")

[`config_dir`](ejudge.xml:config_dir "wikilink") (\*)

[`contests_dir`](ejudge.xml:contests_dir "wikilink") (\*)

[`contests_home_dir`](ejudge.xml:contests_home_dir "wikilink") (\*)

[`contests_ws_port`](ejudge.xml:contests_ws_port "wikilink")

[`default_avatar_plugin`](ejudge.xml:default_avatar_plugin "wikilink")

[`default_clardb_plugin`](ejudge.xml:default_clardb_plugin "wikilink")

[`default_content_plugin`](ejudge.xml:default_content_plugin "wikilink")

[`default_content_url_prefix`](ejudge.xml:default_content_url_prefix "wikilink")

[`default_rundb_plugin`](ejudge.xml:default_rundb_plugin "wikilink")

[`default_status_plugin`](ejudge.xml:default_status_plugin "wikilink")

[`default_variant_plugin`](ejudge.xml:default_variant_plugin "wikilink")

[`default_xuser_plugin`](ejudge.xml:default_xuser_plugin "wikilink")

[`email_program`](ejudge.xml:email_program "wikilink") (\*\*)

[`full_cgi_data_dir`](ejudge.xml:full_cgi_data_dir "wikilink") (\*\*)

[`host_options`](ejudge.xml:host_options "wikilink")

  
[`host`](ejudge.xml:host_options:host "wikilink")

  
[`option`](ejudge.xml:host_options:host:option "wikilink")

[`job_server_log`](ejudge.xml:job_server_log "wikilink") (\*\*)

[`job_server_spool`](ejudge.xml:job_server_spool "wikilink") (\*\*)

[`job_server_work`](ejudge.xml:job_server_work "wikilink") (\*\*)

[`l10n_dir`](ejudge.xml:l10n_dir "wikilink") (\*)

[`max_loaded_contests`](ejudge.xml:max_loaded_contests "wikilink")

[`oauth_user_map`](ejudge.xml:oauth_user_map "wikilink")

  
[`oauth_entry`](ejudge.xml:oauth_entry "wikilink")

[`register_email`](ejudge.xml:register_email "wikilink")

[`register_url`](ejudge.xml:register_url "wikilink")

[`run_path`](ejudge.xml:run_path "wikilink") (\*)

[`script_dir`](ejudge.xml:script_dir "wikilink") (\*)

[`serialization_key`](ejudge.xml:serialization_key "wikilink") (\*\*)

[`serve_path`](ejudge.xml:serve_path "wikilink") (\*)

[`socket_path`](ejudge.xml:socket_path "wikilink") (\*)

[`super_serve_log`](ejudge.xml:super_serve_log "wikilink") (\*\*)

[`super_serve_socket`](ejudge.xml:super_serve_socket "wikilink") (\*)

[`testing_work_dir`](ejudge.xml:testing_work_dir "wikilink") (\*\*)

[`userdb_file`](ejudge.xml:userdb_file "wikilink") (\*\*)

[`userlist_log`](ejudge.xml:userlist_log "wikilink") (\*\*)

[`user_map`](ejudge.xml:user_map "wikilink")

  
[`map`](ejudge.xml:map "wikilink")

[`var_dir`](ejudge.xml:var_dir "wikilink") (\*\*)

(\*) обозначены элементы, не рекомендуемые к явному использованию,
поскольку их значение предпочтительнее задавать при компиляции системы
опциями скрипта [`configure`](configure "wikilink").

(\*\*) Обозначены элементы, корректное значение которых устанавливается
при первоначальной настройке системы `ejudge`, и которые не
рекомендуется изменять в дальнейшем.
