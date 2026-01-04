Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[ejudge.xml](ejudge.xml.md)

Этот конфигурационный файл содержит общие настройки системы ejudge,
которые используются всеми компонентами. Обычно этот файл находится по
пути `/home/judges/data/ejudge.xml`, то есть в подкаталоге `data`
каталога турниров.

### Общая структура

Конфигурационный файл должен быть корректным XML-файлом. Он должен
состоять из единственного элемента первого уровня config. Иерархия
элементов приведена на схеме ниже.

  
[`config`](ejudge.xml:config.md)

  
[`caps`](ejudge.xml:caps.md)

  
[`cap`](ejudge.xml:cap.md)

[`caps_file`](ejudge.xml:caps_file.md)

[`charset`](ejudge.xml:charset.md) (\*)

[`compile_home_dir`](ejudge.xml:compile_home_dir.md) (\*\*)

[`compile_log`](ejudge.xml:compile_log.md) (\*\*)

[`compiler_options`](ejudge.xml:compiler_options.md)

  
[`compiler_option`](ejudge.xml:compiler_option.md)

[`config_dir`](ejudge.xml:config_dir.md) (\*)

[`contests_dir`](ejudge.xml:contests_dir.md) (\*)

[`contests_home_dir`](ejudge.xml:contests_home_dir.md) (\*)

[`contests_ws_port`](ejudge.xml:contests_ws_port.md)

[`default_avatar_plugin`](ejudge.xml:default_avatar_plugin.md)

[`default_clardb_plugin`](ejudge.xml:default_clardb_plugin.md)

[`default_content_plugin`](ejudge.xml:default_content_plugin.md)

[`default_content_url_prefix`](ejudge.xml:default_content_url_prefix.md)

[`default_rundb_plugin`](ejudge.xml:default_rundb_plugin.md)

[`default_status_plugin`](ejudge.xml:default_status_plugin.md)

[`default_variant_plugin`](ejudge.xml:default_variant_plugin.md)

[`default_xuser_plugin`](ejudge.xml:default_xuser_plugin.md)

[`email_program`](ejudge.xml:email_program.md) (\*\*)

[`full_cgi_data_dir`](ejudge.xml:full_cgi_data_dir.md) (\*\*)

[`host_options`](ejudge.xml:host_options.md)

  
[`host`](ejudge.xml:host_options:host.md)

  
[`option`](ejudge.xml:host_options:host:option.md)

[`job_server_log`](ejudge.xml:job_server_log.md) (\*\*)

[`job_server_spool`](ejudge.xml:job_server_spool.md) (\*\*)

[`job_server_work`](ejudge.xml:job_server_work.md) (\*\*)

[`l10n_dir`](ejudge.xml:l10n_dir.md) (\*)

[`max_loaded_contests`](ejudge.xml:max_loaded_contests.md)

[`oauth_user_map`](ejudge.xml:oauth_user_map.md)

  
[`oauth_entry`](ejudge.xml:oauth_entry.md)

[`register_email`](ejudge.xml:register_email.md)

[`register_url`](ejudge.xml:register_url.md)

[`run_path`](ejudge.xml:run_path.md) (\*)

[`script_dir`](ejudge.xml:script_dir.md) (\*)

[`serialization_key`](ejudge.xml:serialization_key.md) (\*\*)

[`serve_path`](ejudge.xml:serve_path.md) (\*)

[`socket_path`](ejudge.xml:socket_path.md) (\*)

[`super_serve_log`](ejudge.xml:super_serve_log.md) (\*\*)

[`super_serve_socket`](ejudge.xml:super_serve_socket.md) (\*)

[`testing_work_dir`](ejudge.xml:testing_work_dir.md) (\*\*)

[`userdb_file`](ejudge.xml:userdb_file.md) (\*\*)

[`userlist_log`](ejudge.xml:userlist_log.md) (\*\*)

[`user_map`](ejudge.xml:user_map.md)

  
[`map`](ejudge.xml:map.md)

[`var_dir`](ejudge.xml:var_dir.md) (\*\*)

(\*) обозначены элементы, не рекомендуемые к явному использованию,
поскольку их значение предпочтительнее задавать при компиляции системы
опциями скрипта [`configure`](configure.md).

(\*\*) Обозначены элементы, корректное значение которых устанавливается
при первоначальной настройке системы `ejudge`, и которые не
рекомендуется изменять в дальнейшем.
