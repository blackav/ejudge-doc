Навигация: [Главная страница](main_Page.md)/[Система
ejudge](система_ejudge.md)/[Инсталляция](инсталляция.md)/[Инсталляция
из исходных
текстов](инсталляция_из_исходных_текстов.md)/[Рекомендуемые
опции configure](рекомендуемые_опции_configure.md)

# Fedora

`./configure --prefix=/opt/ejudge --enable-charset=utf-8 --with-httpd-cgi-bin-dir=/var/www/cgi-bin --with-httpd-htdocs-dir=/var/www/html --enable-ajax --enable-local-dir=/var/lib/ejudge --enable-hidden-server-bins`

# Ubuntu

`./configure --prefix=/opt/ejudge --enable-charset=utf-8 --with-httpd-cgi-bin-dir=/usr/lib/cgi-bin --with-httpd-htdocs-dir=/var/www/html --enable-ajax --enable-local-dir=/var/lib/ejudge --enable-hidden-server-bins`

# Suse

`./configure --prefix=/opt/ejudge --libexecdir=/opt/ejudge/libexec --enable-charset=utf-8 --with-httpd-cgi-bin-dir=/srv/www/cgi-bin --with-httpd-htdocs-dir=/srv/www/htdocs --enable-ajax --enable-local-dir=/var/lib/ejudge --enable-hidden-server-bins`
