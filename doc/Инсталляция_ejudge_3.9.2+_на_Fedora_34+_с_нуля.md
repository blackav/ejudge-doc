Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Инсталляция](Инсталляция "wikilink")/[Инсталляция
ejudge 3.9.2+ на Fedora 34+ с
нуля](Инсталляция_ejudge_3.9.2+_на_Fedora_34+_с_нуля "wikilink")

Данный документ описывает инсталляцию ejudge
[3.10.0](Изменения_в_версии_3.10.0 "wikilink") и более поздних на чистую
систему Fedora 34 и более позних (35, 36). Он отличается от [предыдущей
версии](Инсталляция_ejudge_на_Fedora_с_нуля "wikilink") тем, что убраны
шаги установки и настройки mongo. В качестве базы данных используется
только mariadb (mysql).

Перед началом действий по инсталляции ejudge необходимо
проинсталлировать операционную систему. Для компиляции системы ejudge и
вообще для работы потребуется какой-то непривилегированный пользователь,
назовем его `user`. Создайте его перед началом инсталляции. Кроме того,
в процессе инсталляции будет создано еще несколько пользователей,
которые используются для работы самой ejudge.

Далее все команды, которые необходимо выполнить пользователем `root`
будут обозначены как `#`. Например:

`# dnf update -y`

Все команды, которые необходмо выполнить пользователем `ejudge` будут
обозначены как `[ejudge]$`. Например:

`[ejudge]$ ejudge-configure-compilers`

Все команды, которые необходимо выполнить пользователем `user` будут
обозначены как `[user]$`.

Система ejudge будет исталлироваться в каталог `/opt/ejudge`, а каталог
турниров будет размещаться в `/home/judges`. При желании вы можете
поменять эти пути, тогда соответствующим образом измените команды.

### Первоначальная настройка операционной системы

1\. Установите редактор nano, vim или любой другой.

`# dnf install -y vim nano`

2\. Отключите selinux. Для этого в файле `/etc/selinux/config` найдите
строку, устанавливающую значение `SELINUX`, и отредактируете ее, чтобы
она стала строкой

`SELINUX=disabled`

3\. Для отключения selinux измените опции загрузки

`# grubby --update-kernel ALL --args selinux=0`

4\. Обновите систему

`# dnf update -y`

5\. Перезагрузите систему

`# init 6`

6\. Включите русскую локаль в glibc

`# dnf install -y glibc-locale-source`  
`# localedef -v -c -i ru_RU -f UTF-8 ru_RU.UTF-8`

7\. Установите mariadb

`# dnf install -y mariadb mariadb-connect-engine mariadb-connector-c-devel mariadb-connector-odbc mariadb-devel mariadb-server mariadb-server-utils mariadb-backup mariadb-common mariadb-errmsg`  
`# systemctl enable mariadb`  
`# systemctl start mariadb.service`

8\. Настройте инсталляцию mariadb. Нужно будет задать новый пароль для
пользователя root в mariadb. Обозначим этот пароль как
`MYSQL_ROOT_PASSWORD`

`# mysql_secure_installation`

9\. Установите много разных пакетов с библиотеками и языками
программирования

`# dnf install -y libmongo-client-devel libmongocrypt-devel mongo-c-driver-devel mongo-c-driver-libs libmongocrypt libbson-devel`  
`# dnf install -y httpd httpd-devel httpd-tools`  
`# dnf install -y net-tools wget tar bzip2 p7zip fuse-devel openvpn htop`  
`# dnf install -y make gcc glibc-devel glibc-static bison flex gawk sed file zlib zlib-devel ncurses ncurses-devel expat expat-devel gettext gettext-devel libzip libzip-devel libcurl libcurl-devel libuuid libuuid-devel openssl openssl-devel git tmux bc`  
`# dnf install -y firefox vim screen wget ncftp mc fuse-sshfs patch kernel-tools kernel-devel gcc strace subversion gdb valgrind gcc-c++ libstdc++-static python python3 gcc-gfortran libgfortran-static gcc-go libgo-static nasm libstdc++-devel`  
`# dnf install -y glibc-devel.i686 glibc-static.i686 libstdc++-devel.i686 libstdc++-static.i686`  
`# dnf install -y libtool autoconf automake`  
`# dnf install -y clang clang-devel clang-libs`  
`# dnf install -y fpc ghc gprolog php python2 pypy pypy3 ruby rust scala nodejs swift-lang`  
`# dnf install -y mono-addins-devel mono-basic-devel mono-complete`  
`# dnf install -y dotnet dotnet-runtime-8.0 dotnet-sdk-8.0`  
`# dnf install -y libnfs libnfs-utils libnfsidmap nfs-stats-utils nfs-utils nfswatch  nfs4-acl-tools xz-devel hiredis-devel redis`

10\. Установите и сконфигурируйте golang

`# dnf install -y golang`  
`# alternatives --config go`

Выберите `/usr/lib/golang/bin/go`

11\. Установите и сконфигурируйте java

`# dnf install -y java-latest-openjdk java-latest-openjdk-devel java-latest-openjdk-headless java-latest-openjdk-jmods`  
`# alternatives --config java`

Выберите java-17 или более старшую версию (java-18 и т. д.)

`# alternatives --config javac`

Выберите java-17 или более старшую версию (java-18 и т. д.)

`# alternatives --config java_sdk_openjdk`

Выберите java-17 или более старшую версию (java-18 и т. д.)

`# alternatives --config jre_openjdk`

Выберите java-17 или более старшую версию (java-18 и т. д.)

12\. Установите TypeScript

`# npm install -g ts-node`

13\. Настройте обработку core dumps

`# cat <`<EOF >` /etc/sysctl.d/51-coredump.conf`  
`kernel.core_pattern=core`  
`fs.suid_dumpable=0`  
`EOF`

`# vim /etc/systemd/coredump.conf`

В секции `[Coredump]` должно быть `Storage=none`

14\. Создание пользователей для ejudge

`# adduser -c 'ejudge user' -s /bin/bash ejudge`  
`# adduser -c 'ejudge executor' -d / -M -s /sbin/nologin ejexec`  
`# adduser -c 'ejudge executor 1' -d / -M -s /sbin/nologin ejexec1`  
`# adduser -c 'ejudge executor 2' -d / -M -s /sbin/nologin ejexec2`  
`# adduser -c 'ejudge executor 3' -d / -M -s /sbin/nologin ejexec3`  
`# adduser -c 'ejudge compiler' -d /home/judges/compile -M -s /sbin/nologin ejcompile`  
`# usermod -a -G ejcompile ejudge`

Скорее всего еще потребуется настроить вход в пользователя ejudge без
пароля с помощью ключей ssh.

15\. Создание каталогов

`# mkdir /opt/ejudge`  
`# chown user:user /opt/ejudge`  
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
`# mkdir /var/log/ejudge`  
`# chown ejudge:ejudge /var/log/ejudge`  
`# cd /home/judges; ln -s /var/log/ejudge var`

16\. Компиляция ejudge

`[user]$ cd`  
`[user]$ git clone `[`https://github.com/blackav/ejudge.git`](https://github.com/blackav/ejudge.git)  
`[user]$ cd ejudge`  
`[user]$ ./configure --prefix=/opt/ejudge --enable-charset=utf-8 --with-httpd-cgi-bin-dir=/var/www/cgi-bin --with-httpd-htdocs-dir=/var/www/html --enable-ajax --enable-local-dir=/var/lib/ejudge --enable-hidden-server-bins --with-primary-user=ejudge --with-exec-user=ejexec --with-compile-user=ejcompile --enable-compile-spool-dir --enable-run-spool-dir --enable-contests-status-dir`  
`[user]$ make`  
`[user]$ make install`

17\. Настройка прав

`# /opt/ejudge/bin/ejudge-suid-setup`  
`# /opt/ejudge/bin/ejudge-upgrade-web`

18\. Настройка httpd

`# vim /etc/httpd/conf/httpd.conf`

В этом файле найдите строку `ScriptAlias /cgi-bin/ "/var/www/cgi-bin/"`.
После нее допишите текст:

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

Найдите строку `<Directory "/var/www/cgi-bin">`. Отредактируйте
дальнейший текст, чтобы он был таким:

`<Directory "/var/www/cgi-bin">`  
`    AllowOverride None`  
`    Options FollowSymLinks`  
`    Require all granted`  
</Directory>

После этой строки добавьте:

`SetEnvIfNoCase ^Authorization$ "(.+)" HTTP_AUTHORIZATION=$1`

19\. Запустите httpd

`# systemctl enable httpd`  
`# systemctl start httpd`

20\. Создайте базу данных ejudge

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

21\. Запустите конфигуратор ejudge

`[ejudge]$ cd`  
`[ejudge]$ /opt/ejudge/bin/ejudge-setup`

В разделе 'Edit global settings' в поле 'Sendmail program' введите
`/bin/false`, если там ничего нет. Это поле будет отмечено
восклицательным знаком.

В разделе 'Edit MySQL settings' в поле 'User password' введите пароль
пользователя ejudge от MySQL (см. предыдущий шаг).

После этого выполните 'Save setup script', назовите его
`ejudge-install.sh`, и выйдите из программы конфигурирования.

22\. Запустите установочный скрипт

`# ~ejudge/ejudge-install.sh`

23\. Еще раз обновите языки программирования

`[ejudge]$ /opt/ejudge/bin/ejudge-configure-compilers`

24\. Донастройте конфигурационный файл ejudge.xml.

`[ejudge]$ vim /home/judges/data/ejudge.xml`

Пропишите плагины хранения данных по умолчанию.

`  `<default_rundb_plugin>`mysql`</default_rundb_plugin>  
`  `<default_clardb_plugin>`mysql`</default_clardb_plugin>  
`  `<default_status_plugin>`mysql`</default_status_plugin>  
`  `<default_avatar_plugin>`mysql`</default_avatar_plugin>  
`  `<default_xuser_plugin>`mysql`</default_xuser_plugin>  
`  `<default_variant_plugin>`mysql`</default_variant_plugin>

Убедитесь, что плагины настроены правильно:

`   `<plugin type="common" name="mysql" load="yes">  
`     `<config>  
`       `<password_file>`mysql_password`</password_file>  
`       `<database>`ejudge`</database>  
`     `</config>  
`   `</plugin>  
`   `<plugin type="uldb" name="mysql" load="yes" default="yes">  
`     `<config/>  
`   `</plugin>  
`   `<plugin type="cldb" name="mysql" load="yes">  
`     `<config/>  
`   `</plugin>  
`   `<plugin type="rldb" name="mysql" load="yes">  
`     `<config/>  
`   `</plugin>  
`   `<plugin type="xuser" name="mysql" load="yes">  
`     `<config/>  
`   `</plugin>  
`   `<plugin type="avatar" name="mysql" load="yes">  
`     `<config/>  
`   `</plugin>  
`   `<plugin type="status" name="mysql" load="yes">  
`     `<config/>  
`   `</plugin>  
`   `<plugin type="variant" name="mysql" load="yes">  
`     `<config/>  
`   `</plugin>

25\. Все сделано, можно запускать ejudge

`[ejudge]$ /opt/ejudge/bin/ejudge-control start`
