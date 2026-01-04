Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
языков](serve.cfg:language "wikilink")/[`disable_auto_update`](Serve.cfg:language:disable_auto_update "wikilink")

Данный конфигурационный параметр предназначен для использования в
конфигурационном файле `compile.cfg` компонента
[ej-compile](ej-compile "wikilink"). Он запрещает обновление
конфигурации данного языка программирования программой
[ejudge-configure-compilers](ejudge-configure-compilers "wikilink").
Конфигурационный параметр полезен, когда в файл compile.cfg были внесены
ручные изменения, и нежелательно, чтобы эти изменения были затерты
программой ejudge-configure-compilers.

Поддерживается начиная с версии
[3.13.0](изменения_в_версии_3.13.0 "wikilink").
