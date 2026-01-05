Навигация: [Главная страница](main_Page.md)/[Система
ejudge](система_ejudge.md)/[Инсталляция](инсталляция.md)/[Инсталляция
ejudge 3.10.0+ на Ubuntu 22.04 с
нуля](инсталляция_ejudge_3.10.0+_на_Ubuntu_22.04_с_нуля.md)

Данный документ описывает инсталляцию ejudge
[3.10.0](изменения_в_версии_3.10.0.md) и более поздних на чистую
систему Ubuntu 22.04.1. В качестве базы данных используется только
mariadb (mysql).

Перед началом действий по инсталляции ejudge необходимо
проинсталлировать операционную систему. В процессе инсталляции системы
потребуется создать непривилегированного пользователя, назовем его
`ubuntu`. Этот пользователь имеет право выполнять команду `sudo` для
запуска команд с правами пользователя `root`.

Кроме того, в процессе инсталляции будет создано еще несколько
пользователей, которые используются для работы самой ejudge.

Далее все команды, которые необходимо выполнить пользователем `root`
будут обозначены как `#`. Например:

`# apt-get update -y`

Можно запускать команды с правами `root` по отдельности с помощью sudo,
например:

`[ubuntu]$ sudo apt-get update -y`

Но можно один раз запустить командную оболочку под пользователем `root`
и использовать ее.

`[ubuntu]$ sudo bash`

Все команды, которые необходмо выполнить пользователем `ejudge` будут
обозначены как `[ejudge]$`. Например:

`[ejudge]$ ejudge-configure-compilers`

Все команды, которые необходимо выполнить пользователем `ubuntu` будут
обозначены как `[ubuntu]$`.

Система ejudge будет исталлироваться в каталог `/opt/ejudge`, а каталог
турниров будет размещаться в `/home/judges`. При желании вы можете
поменять эти пути, тогда соответствующим образом измените команды.

### Первоначальная настройка операционной системы

1\. Обновите систему

`# apt-get update`  
`# apt-get dist-upgrade -y`

2\. Установите необходимые пакеты

`# apt-get install -y net-tools wget tar bzip2 p7zip openvpn htop make gcc bison flex gawk sed file expat libexpat-dev gettext libzip-dev libcurl4-openssl-dev openssl git tmux bc gcc g++ locales-all mariadb-client mariadb-server mycli libbson-dev libmongoc-dev fuse libfuse-dev zlib1g-dev ncurses-base ncurses-bin ncurses-term libncurses-dev expat libexpat1-dev gettext-el libgettextpo-dev zip libzip-dev uuid uuid-dev vim screen wget mc gcc strace subversion gdb python2 python3 nasm libtool autoconf automake clang libelf-dev libmysqlclient-dev pkg-config liblzma-dev gcc-multilib apache2 apache2-utils libhiredis-dev`

3\. Активируйте mariadb

`# systemctl enable mariadb`  
`# systemctl start mariadb`

4\. Задайте пароль администратора (root) в mariadb. Обозначим этот
пароль как `MYSQL_ROOT_PASSWORD`

`# mysql_secure_installation`

5\. Создайте пользователей

`# useradd -c 'ejudge user' -m -s /bin/bash ejudge`  
`# useradd -c 'ejudge executor' -d / -M -s /sbin/nologin ejexec`  
`# useradd -c 'ejudge executor 1' -d / -M -s /sbin/nologin ejexec1`  
`# useradd -c 'ejudge executor 2' -d / -M -s /sbin/nologin ejexec2`  
`# useradd -c 'ejudge executor 3' -d / -M -s /sbin/nologin ejexec3`  
`# useradd -c 'ejudge compiler' -d /home/judges/compile -M -s /sbin/nologin ejcompile`  
`# adduser ejudge ejcompile`

6\. Создайте каталоги

`# mkdir /opt/ejudge`  
`# chown ubuntu:ubuntu /opt/ejudge`  
`# mkdir /home/judges`  
`# chown ejudge:ejudge /home/judges`  
`# mkdir /home/ej-compile-spool`  
`# chown ejudge:ejcompile /home/ej-compile-spool`  
`# chmod 6775 /home/ej-compile-spool`  
`# mkdir /home/ej-run-spool`  
`# chown ejudge:ejudge /home/ej-run-spool`  
`# chmod 755 /home/ej-run-spool`  
`# mkdir /var/lib/ejudge`  
`# chown ejudge:ejudge /var/lib/ejudge`

7\. Настройте apache httpd

`# mkdir /var/www/cgi-bin`  
`# cd /etc/apache2/mods-enabled`  
`# ln -s ../mods-available/cgi.load .`  
`# cd ../conf-enabled`

8\. В файл `/etc/apache2/conf-enabled/serve-cgi-bin.conf` запишите
следующее содержимое:

`ScriptAlias /cgi-bin/ /var/www/cgi-bin/`  
`<Directory "/var/www/cgi-bin">`  
`    AllowOverride None`  
`    Options +ExecCGI +FollowSymLinks`  
`    Require all granted`  
</Directory>

9\. Отредактируйте файл `/etc/apache2/sites-enabled/000-default.conf`
чтобы перед строкой `</VirtualHost` были строки:

`     ScriptAlias /master   "/var/www/cgi-bin/new-master"`  
`     ScriptAlias /client   "/var/www/cgi-bin/new-client"`  
`     ScriptAlias /new-judge "/var/www/cgi-bin/new-judge"`  
`     ScriptAlias /new-master "/var/www/cgi-bin/new-master"`  
`     ScriptAlias /new-client "/var/www/cgi-bin/new-client"`  
`     ScriptAlias /judge    "/var/www/cgi-bin/new-judge"`  
`     ScriptAlias /serve-control "/var/www/cgi-bin/serve-control"`  
`     ScriptAlias /users    "/var/www/cgi-bin/users"`  
`     ScriptAlias /register "/var/www/cgi-bin/new-register"`  
`     ScriptAlias /new-register "/var/www/cgi-bin/new-register"`  
`     ScriptAliasMatch ^/ej/.+ /var/www/cgi-bin/new-client`

10\. Активируйте apache2

`# systemctl enable apache2`  
`# systemctl start apache2`

11\. Перезагрузите систему

`# reboot`

### Компиляция и настройка ejudge

12\. Компиляция ejudge

`[ubuntu]$ cd`  
`[ubuntu]$ git clone `[`https://github.com/blackav/ejudge.git`](https://github.com/blackav/ejudge.git)  
`[ubuntu]$ cd ejudge`  
`[ubuntu]$ ./configure --prefix=/opt/ejudge --enable-charset=utf-8 --with-httpd-cgi-bin-dir=/var/www/cgi-bin --with-httpd-htdocs-dir=/var/www/html --enable-ajax --enable-local-dir=/var/lib/ejudge --enable-hidden-server-bins --with-primary-user=ejudge --with-exec-user=ejexec --with-compile-user=ejcompile --enable-compile-spool-dir --enable-run-spool-dir --enable-contests-status-dir`  
`[ubuntu]$ make`  
`[ubuntu]$ make install`

13\. Настройка прав

`# /opt/ejudge/bin/ejudge-suid-setup`  
`# /opt/ejudge/bin/ejudge-upgrade-web`

14\. Создайте базу данных ejudge

`# mysql -p`

Введите пароль пользователя `root` от mysql.

`Enter password: ******`

В командной строке mysql создайте базу ejudge и пользователя ejudge

`MariaDB [(none)]> create user 'ejudge'@'localhost' identified by 'PASSWORD';`  
`` MariaDB [(none)]> create database `ejudge`; ``  
`` MariaDB [(none)]> grant all on `ejudge` . * to 'ejudge'@'localhost'; ``  
`MariaDB [(none)]> flush privileges;`

Здесь `PASSWORD` это пароль для пользователя ejudge в БД. Он потребуется
на следующем шаге.

15\. Запустите конфигуратор ejudge

`[ejudge]$ cd`  
`[ejudge]$ /opt/ejudge/bin/ejudge-setup`

В разделе 'Edit MySQL settings' в поле 'User password' введите пароль
пользователя ejudge от MySQL (см. предыдущий шаг).

После этого выполните 'Save setup script', назовите его
`ejudge-install.sh`, и выйдите из программы конфигурирования.

16\. Запустите установочный скрипт

`# ~ejudge/ejudge-install.sh`

17\. Еще раз обновите языки программирования

`[ejudge]$ /opt/ejudge/bin/ejudge-configure-compilers`

18\. Исправьте права на каталог компиляции

`# chgrp ejcompile /home/ej-compile-spool`

19\. Все сделано, можно запускать ejudge

`[ejudge]$ /opt/ejudge/bin/ejudge-control start`

Административный интерфейс должен быть доступен по URL
[`http://localhost/serve-control`](http://localhost/serve-control).
Пользователь `ejudge`, пароль `ejudge`.
