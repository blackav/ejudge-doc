Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Инсталляция](Инсталляция "wikilink")/[Инсталляция
из исходных
текстов](Инсталляция_из_исходных_текстов "wikilink")/[Рекомендуемые
опции configure](Рекомендуемые_опции_configure "wikilink")

# Fedora

`./configure --prefix=/opt/ejudge --enable-charset=utf-8 --with-httpd-cgi-bin-dir=/var/www/cgi-bin --with-httpd-htdocs-dir=/var/www/html --enable-ajax --enable-local-dir=/var/lib/ejudge --enable-hidden-server-bins`

# Ubuntu

`./configure --prefix=/opt/ejudge --enable-charset=utf-8 --with-httpd-cgi-bin-dir=/usr/lib/cgi-bin --with-httpd-htdocs-dir=/var/www/html --enable-ajax --enable-local-dir=/var/lib/ejudge --enable-hidden-server-bins`

# Suse

`./configure --prefix=/opt/ejudge --libexecdir=/opt/ejudge/libexec --enable-charset=utf-8 --with-httpd-cgi-bin-dir=/srv/www/cgi-bin --with-httpd-htdocs-dir=/srv/www/htdocs --enable-ajax --enable-local-dir=/var/lib/ejudge --enable-hidden-server-bins`
