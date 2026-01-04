Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Инсталляция](Инсталляция "wikilink")/[Инсталляция
на ALT Linux](Инсталляция_на_ALT_Linux "wikilink")/[Настройка базы
данных
MySQL](Инсталляция_на_ALT_Linux:Настройка_базы_данных_MySQL "wikilink")

Система ejudge использует сервер баз данных MySQL для хранения базы
пользователей и сданных решений.

В дистрибутивах ALT Linux вместо базы MySQL может использоваться база
mariadb. Настройка mariadb производится так же (в том числе консольная
команда для запуска клиента называется mysql).

Перед запуском ejudge необходимо создать в MySQL пользователя и базу
данных.

Запустите сервис MySQL и консольный клиент MySQL:

`# service mysqld start`  
`# mysql`

В консольном клиенте MySQL выполните следующие команды:

`mysql> CREATE DATABASE ejudge;`  
`mysql> CREATE USER 'ejudge'@'localhost' IDENTIFIED BY 'ejudge';`  
`mysql> GRANT ALL ON ejudge.* TO 'ejudge'@'localhost';`

Во второй команде желательно заменить пароль пользователя базы данных
ejudge на сложную комбинацию.
