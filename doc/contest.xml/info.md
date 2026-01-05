Навигация: [Главная страница](../main_Page.md)/[Система
ejudge](../система_ejudge.md)/[Использование](../использование.md)/[Конфигурационные
файлы](../конфигурационные_файлы.md)/[contest.xml](../contest.xml.md)/[Общая
информация](info.md)

В системе `ejudge` описание каждого турнира хранится в отдельном
XML-файле. Все файлы располагаются в одном каталоге, который задаётся в
элементе `contests_dir` для конфигурационных файлов в формате XML или в
параметре `contests_dir` для конфигурационных файлов в формате INI.
Описание каждого турнира хранится в этом каталоге в файле с именем
*N*`.xml`, где *N* — идентификатор (номер) турнира в десятичной записи
из 6 знаков с ведущими нулями. Например, информация о турнире с номером
1 хранится в файле `000001.xml`, а информация о турнире с номером 192 —
в файле `000192.xml`. Идентификатор турнира назначается администратором
системы `ejudge` и должен быть целым числом в диапазоне *1 ≤ N ≤
999999*. Никакие два турнира в одной инсталляции системы `ejudge` не
могут иметь один и тот же идентификатор. Для большей эффективности
работы системы `ejudge` рекомендуется нумеровать турниры подряд, начиная
с 1. Идентификатор турнира, определяемый по имени файла, в котором
хранится его описание, должен совпадать со значением атрибута id
элемента верхнего уровня `contest` самого файла.

Файл описания турнира должен представлять собой правильно сформированный
XML-файл. Элементом верхнего уровня файла является элемент `contest`,
который должен присутствовать и не может повторяться. Общая структура
вложенности элементов файла приведена ниже: <tt>

  
contest

  
  
name

name_en

register_access

  
ip

users_access

  
ip

master_access

  
ip

judge_access

  
ip

team_access

  
ip

serve_control_access

  
ip

field

contestants

  
field

reserves

  
field

coaches

  
field

advisors

  
field

guests

  
field

users_header_file

users_footer_file

register_header_file

register_footer_file

team_header_file

team_footer_file

register_email

register_url

register_email_file

team_url

registration_deadline

users_head_style

users_par_style

users_table_style

users_verb_style

register_head_style

register_par_style

register_table_style

team_head_style

team_par_style

<!-- -->

  
  
caps

  
cap

root_dir

conf_dir

standings_url

problems_url

client_flags

serve_user

serve_group

run_user

run_group

users_table_format

users_table_format_en

users_table_legend

users_table_legend_en

user_name_comment

allowed_languages

cf_notify_email

clar_notify_email

daily_stat_email</tt>

В конфигурационном файле турнира, в частности, задаются дополнительные
ограничения на допустимые IP-адреса для всех CGI-программ. Кроме этого,
в конфигурационном файле определяются обязательные и необязательные поля
анкеты участника.
