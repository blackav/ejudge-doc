Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Инсталляция](Инсталляция.md)/[Настройка
использования MySQL](Настройка_использования_MySQL.md)

<b>Начиная с версии 2.3.29 настройка хранения данных в MySQL выполняется
автоматически, если поддержка MySQL была включена при компиляции.</b>

Включение использования MySQL для хранения информации о пользователях и
посылках следует выполнять после того, как настроена базовая инсталляция
ejudge и проверена ее работоспособность. При компиляции ejudge должны
быть обнаружены библиотеки MySQL и скомпилированы соответствующие
плагины. Например, на системе Fedora для этого должны быть установлены
пакеты mysql, mysql-devel, mysql-libs.

Предположим, что каталоги с турнирами и конфигурационными файлами ejudge
размещаются в каталоге /home/judges. В этом случае основной
конфигурационный файл ejudge называется /home/judges/data/ejudge.xml.

Выполните следующие шаги:

1\. Создайте базу данных и пользователя с полными правами для этой базы
данных. Предположим, что база данных называется ejudge, пользователь
тоже называется ejudge, а его пароль - EjudgePassword. <b>Не
устанавливайте этот пароль в реальных базах данных!</b>

`CREATE USER 'ejudge'@'%' IDENTIFIED BY 'ejudge';`  
`GRANT USAGE ON * . * TO 'ejudge'@'%' IDENTIFIED BY 'ejudge' WITH MAX_QUERIES_PER_HOUR 0 MAX_CONNECTIONS_PER_HOUR 0 MAX_UPDATES_PER_HOUR 0 MAX_USER_CONNECTIONS 0 ;`  
`` CREATE DATABASE IF NOT EXISTS `ejudge` ; ``  
`` GRANT ALL PRIVILEGES ON `ejudge` . * TO 'ejudge'@'%'; ``

2\. Остановите ejudge, если система ejudge запущена.

`ejudge-control stop`

3\. Создайте файл /home/judges/data/mysql_password со следующего вида:

`ejudge`  
`EjudgePassword`

Первая строка файла - это имя пользователя базы данных, вторая строка
файла - его пароль.

4\. Следует сделать этот файл доступным на чтение только пользователю,
из-под которого работает ejudge. Например, если ejudge запускается
из-под пользователя ejudge, то можно выполнить следующую команду, войдя
под пользователем ejudge.

`chmod 600 /home/judges/data/mysql_password`

5\. В файл /home/judges/data/ejudge.xml следует добавить следующие
строки:

`  `<plugins>  
`    `  
`    `<plugin type="nsdb" name="files">  
`      `<config>  
`        `<data_dir>`/home/judges/data/nsdb_files`</data_dir>  
`      `</config>  
`    `</plugin>  
`    `  
`    `<plugin type="common" name="mysql" load="yes">  
`      `<config>  
`        `<password_file>`mysql_password`</password_file>  
`        `<database>`ejudge`</database>  
`      `</config>  
`    `</plugin>  
`    `<plugin type="uldb" name="mysql" load="yes" default="yes">  
`      `<config/>  
`    `</plugin>  
`    `<plugin type="cldb" name="mysql" load="yes">  
`      `<config/>  
`    `</plugin>  
`    `<plugin type="rldb" name="mysql" load="yes">  
`      `<config/>  
`    `</plugin>  
`  `</plugins>

6\. Чтобы для хранения посылок турниров mysql использовался по
умолчанию, в файл /home/judges/data/ejudge.xml следуюет добавить
следующие строки.

`  `<default_rundb_plugin>`mysql`</default_rundb_plugin>  
`  `<default_clardb_plugin>`mysql`</default_clardb_plugin>

7\. Сконвертируйте существующих пользователей

`ej-users --convert --from-plugin xml --to-plugin mysql`

8\. Если были проведены турниры, то базы данных турниров могут быть
сконвертированы с помощью команды:

`ej-convert-runs CNTS-ID file mysql`

9\. Базы вопросов конвертируются командой:

`ej-convert-clars CNTS-ID file mysql`

10\. Систему ejudge можно запустить, будет использоваться база данных
MySQL
