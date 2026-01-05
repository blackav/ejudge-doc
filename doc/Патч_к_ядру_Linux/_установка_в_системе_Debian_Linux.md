Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Патч к ядру
Linux](Патч_к_ядру_Linux.md)/[Патч к ядру Linux: установка в
системе Debian
Linux](Патч_к_ядру_Linux:_установка_в_системе_Debian_Linux.md)

Предполагается, что все нижеописанные действия выполняются из-под
пользователя **root**

Что бы установить патч, понадобится перекомпилировать ядро.

Для этого нужен пакет *make-kpkg* из репозитория debian:

` # apt-get install make-kpkg`

Так же потребуются исходные коды самого ядра linux. Их можно скачать с
kernel.org. Например, версию 2.6.26.3

` # cd /usr/src`  
` # wget `[`http://www.kernel.org/pub/linux/kernel/v2.6/linux-2.6.26.3.tar.bz2`](http://www.kernel.org/pub/linux/kernel/v2.6/linux-2.6.26.3.tar.bz2)

Далее нужно распаковать исходные коды, скачать и применить патч для
нужной версии kernel:

` # tar -xvzf `[`http://www.kernel.org/pub/linux/kernel/v2.6/linux-2.6.26.3.tar.bz2`](http://www.kernel.org/pub/linux/kernel/v2.6/linux-2.6.26.3.tar.bz2)  
` # cd linux-2.6.26.3`  
` # wget `[`http://www.ejudge.ru/download/linux-2.6.26.3-2.6.26.3-cher1.diff`](http://www.ejudge.ru/download/linux-2.6.26.3-2.6.26.3-cher1.diff)  
` # patch -p1 < linux-2.6.26.3-2.6.26.3-cher1.diff`

Можно и желательно так же скопировать конфигурационный файл от текущего
ядра, он находится в папке /boot/ и начинается с "config-"

` # cp /boot/config-ВЕРСИЯ-ЯДРА ./.config`

Заодно можно донастроить конфигурационный файл, вызвав:

` # make menuconfig`

Затем выбрать пункт "*Load Alternate Config File*" ввести ".config"

Не стоит забывать после окончания настройки сохранить .config через
пункт "*Save Alternate Config File*"

Теперь можно приступать к компиляции. Для этого используется make-kpkg

` # make-kpkg --initrd kernel_image kernel_headers`

Для ускорения компиляции можно добавить параметр **CONCURRENCY_LEVEL** -
количество одновременных компиляций. Он должен быть равен числу ядер в
процессоре плюс 1 или 2:

Для двуядерного процессора стоит писать:

` # CONCURRENCY_LEVEL=3 make-kpkg --initrd kernel_image kernel_headers`

*Строго запрещается задавать параметр "-jX" в переменной CC, если вы её
меняете. Иначе ядро может просто не скомпилироваться!*

Осталось лишь установить ядро:

` # cd ..`  
` # dpkg --install linux-headers-2.6.26.3* linux-image-2.6.26.3*`

Это автоматически добавит в ваш GRUB или LILO новый пункт с новым ядром.

Остается только перезагрузиться в новое ядро.
