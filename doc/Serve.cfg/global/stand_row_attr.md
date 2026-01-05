Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Глобальные
конфигурационные
параметры](serve.cfg:global.md)/[`stand_row_attr`](Serve.cfg:global:stand_row_attr.md)

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Global settings (serve.cfg)"*, блок *"Standings table attributes"*,
поле *"Standings row attributes"*.

Переменная позволяет определять атрибуты строк таблицы. Эти атрибуты
используются, когда к строке таблицы неприменимы другие атрибуты,
задаваемые глобальными конфигурационными переменными
[`stand_v_row_attr`](serve.cfg:global:stand_v_row_attr.md),
[`stand_r_row_attr`](serve.cfg:global:stand_r_row_attr.md),
[`stand_u_row_attr`](serve.cfg:global:stand_u_row_attr.md),
[`stand_self_row_attr`](serve.cfg:global:stand_self_row_attr.md),
[`stand_contestant_status_attr`](serve.cfg:global:stand_contestant_status_attr.md).

Конфигурационная переменная `stand_row_attr` должна быть определена либо
5, либо 6 раз, задавая таким образом массив из 5 или 6 атрибутов. Массив
используется следующим образом:

- `stand_row_attr[0]` - это атрибут строки заголовка таблицы,
- `stand_row_attr[1]`, `stand_row_attr[2]` - атрибуты четных и нечетных
  строк таблицы соответственно,
- `stand_row_attr[3]`, `stand_row_attr[4]` - атрибуты четных и нечетных
  строк таблицы соответственно, эти две группы атрибутов используются
  попеременно при изменении количества решенных задач у команд.
- `stand_row_attr[5]` (если определен) - атрибуты строк таблицы, в
  которых отображается суммарная информация по всем участникам

турнира.

**Пример.**

`stand_row_attr = " bgcolor=\"#cccccc\" valign=\"top\""`  
`stand_row_attr = " bgcolor=\"#eeffff\" valign=\"top\""`  
`stand_row_attr = " bgcolor=\"#ddffff\" valign=\"top\""`  
`stand_row_attr = " bgcolor=\"#ffeeff\" valign=\"top\""`  
`stand_row_attr = " bgcolor=\"#ffddff\" valign=\"top\""`  
`stand_row_attr = " bgcolor=\"#cccccc\" valign=\"top\""`

Для совместимости со стандартным видом таблицы в предыдущих версиях
системы, если ни глобальная конфигурационная переменная
[`stand_table_attr`](serve.cfg:global:stand_table_attr.md), ни
глобальная конфигурационная переменная
[`stand_row_attr`](serve.cfg:global:stand_row_attr.md) не
установлена, переменная `stand_row_attr` устанавливается в значение "
border=\\1\\".
