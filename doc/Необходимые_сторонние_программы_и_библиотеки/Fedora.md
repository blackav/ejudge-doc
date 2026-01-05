Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Инсталляция](Инсталляция.md)/[Инсталляция
из исходных
текстов](Инсталляция_из_исходных_текстов.md)/[Необходимые
сторонние программы и
библиотеки](Необходимые_сторонние_программы_и_библиотеки.md)/[Fedora,RHEL,CentOS](Необходимые_сторонние_программы_и_библиотеки:Fedora.md)

- <b>make</b>
- <b>gcc</b>
- <b>glibc-devel</b>, <b>glibc-static</b>
- <b>bison</b>
- <b>flex</b>
- <b>gawk</b>, <b>sed</b>
- <b>zlib</b>, <b>zlib-devel</b>
- <b>ncurses</b>, <b>ncurses-devel</b>
- <b>expat</b>, <b>expat-devel</b>
- <b>gettext</b>, <b>gettext-devel</b>
- <b>libzip</b>, <b>libzip-devel</b>
- <b>mysql-libs</b>, <b>mysql</b>, <b>mysql-devel</b>
- <b>libcurl</b>, <b>libcurl-devel</b>
- <b>libuuid</b>, <b>libuuid-devel</b>
- <b>elfutils-libelf-devel</b>, <b>elfutils-libelf-devel-static</b>,
  <b>elfutils-libelf</b>
- <b>mongo-tools</b>, <b>libmongo-client</b>,
  <b>libmongo-client-doc</b>, <b>libmongo-client-devel</b>,
  <b>mongodb-server</b>, <b>mongodb</b>, <b>mongo-tools-devel</b>,
  <b>mongo-cxx-driver-devel</b>
- <b>mariadb</b>, <b>mariadb-server</b>, <b>mariadb-devel</b>,
  <b>mariadb-libs</b>, <b>mariadb-common</b>,
  <b>mariadb-connector-c-devel</b>, <b>mariadb-common</b>,
  <b>mariadb-config</b>, <b>mariadb-errmsg</b>

Дополнительные компиляторы и интерпретаторы языков программирования:

- <b>gcc-c++</b>, <b>libstdc++-static</b>
- <b>fpc</b>
- <b>ruby</b>
- <b>python</b>
- <b>python3</b>
- <b>php</b>, <b>php-common</b>, <b>php-cli</b>
- <b>perl</b>
- <b>gprolog</b>
- <b>mono-core</b>, <b>mono-basic</b>
- <b>java-1.7.0-openjdk</b>, <b>java-1.7.0-openjdk-devel</b> или
  <b>java-1.8.0-openjdk</b>, <b>java-1.8.0-openjdk-devel</b>
- <b>gcc-gfortran</b>

Прочее

`yum install firefox vim screen wget ncftp mc fuse-sshfs patch kernel-tools kernel-devel gcc strace subversion gdb`

Поддержка 32-битных компиляторов на 64-битной платформе:

`yum install glibc-devel.i686 libgcc.i686 libstdc++-devel.i686`

Скрипт для инсталляции всех необходимых пакетов в Fedora 23 i686:
[fedora-install-packages-i686](https://ejudge.ru/download/fedora-install-packages-i686)
