Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Инсталляция](Инсталляция "wikilink")/[Добавление
Borland Kylix](Добавление_Borland_Kylix "wikilink")

Использование Borland Kylix не рекомендуется, так как этот продукт не
развивается и не поддерживается. Вместо него используйте Free Pascal,
хотя он и имеет ряд ошибок, из-за которых программы, нормально
работающие на Kylix, не работают на Free Pascal.

Borland Kylix - это попытка фирмы Borland перенести среду разработки
программ Delphi 7 в операционные системы семейства Linux. Среда
разработки программ (IDE) не работоспособна в современных версиях Linux,
но консольный компилятор (dcc) вполне функционален, хотя некоторые
библиотеки (например, Classes) не работают.

Для использования Borland Kylix в ejudge проинсталлируйте его и добавьте
в переменную PATH путь к скриптам запуска исполняемых файлов (dcc и т.
д.). При инсталляции в /usr/local переменную PATH можно не
модифицировать. После инсталляции Kylix выполните переконфигурирование
компиляторов с помощью ejudge-configure-compilers. Компилятор dcc должен
быть подключен автоматически.

## Возможные ошибки и их решение

При инсталляции Kylix скорее всего не сможет найти необходимые для
работы GUI библиотеки, при этом установка прервется. Чтобы ее
продолжить, необходимо в файле setup.sh после объявлений функций
CheckGtk, CheckJpeg, CheckX

`function CheckGtk {`

`function CheckJpeg {`

`function CheckX {`

дописать

`return 0`

------------------------------------------------------------------------

Если при попытке скомпилировать любой файл с помощью dcc компиляция
прерывается с следующей ошибкой

`Borland Delphi for Linux Version 14.5`  
`Copyright (c) 1983,2002 Borland Software Corporation`  
`Warning: No configuration files found`  
`prog.pas(1) Fatal: Unit not found: 'System.pas' or binary equivalents (DCU,DPU)`

то следует создать файл **/usr/local/etc/dcc.conf** с приблизительно
следующим содержимым:

`--msgcatalog=/usr/local/kylix3/bin`  
`-u/usr/local/kylix3/lib`  
`-o/usr/local/kylix3/bin`

Либо создать папку /usr/local/etc и переустановить Kylix.
