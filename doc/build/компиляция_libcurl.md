# Компиляция libcurl

Навигация: [Главная страница](../main_Page.md)/[Система ejudge](../система_ejudge.md)/[Инсталляция](../инсталляция.md)/[Компиляция библиотеки libcurl](компиляция_libcurl.md)

```bash
wget https://curl.se/download/curl-8.17.0.tar.bz2
tar xf curl-8.17.0.tar.bz2
cd curl-8.17.0/
./configure --prefix=/usr --with-openssl --without-libpsl
make
```
