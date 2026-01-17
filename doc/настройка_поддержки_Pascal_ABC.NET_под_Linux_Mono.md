Навигация: [Главная страница](main_Page.md)/[Система
ejudge](система_ejudge.md)/[Инсталляция](инсталляция.md)/[Настройка
поддержки Pascal ABC.NET под Linux
Mono](настройка_поддержки_Pascal_ABC.NET_под_Linux_Mono.md)

Для работы PascalABC.NET в среде Linux/Mono должен быть установлен Mono
с пакетом дополнительных локализаций. В операционной системе Fedora
необходимо установить пакеты mono-core и mono-locale-extras.

1\. Скачайте с сайта [pascalabc.net](http://pascalabc.net) консольный
компилятор - архив
[PABCNETC.zip](http://pascalabc.net/downloads/PABCNETC.zip)

2\. Разархивируйте его в каталог /usr/local/pasabc - в каталоге
/usr/local/pasabc должен находится файл pabcnetc.exe.

3\. Запустите ejudge-configure-compilers, компилятор pasabc-linux должен
обнаружиться автоматически.

Реализация некоторых стандартных функций PascalABC.NET, таких как
readln, некорректно работает с файлами с концами строк в стиле Unix.
Поэтому рекомендуется при тестировании программ на pasabc-linux
выполнять конвертацию файлов из формата Unix в формат DOS. Для этого в
секции конфигурации языка программирования устанавливается параметр
[`is_dos`](serve.cfg/language/is_dos.md).

Данный компилятор поддерживается, начиная с версии
[2.3.27](change/изменения_в_версии_2.3.27.md).
