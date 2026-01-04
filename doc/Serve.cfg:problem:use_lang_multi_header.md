Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[`use_lang_multi_header`](serve.cfg:problem:use_lang_multi_header "wikilink")

Данная переменная действует, только если включен режим [потестовой
компиляции](потестовая_компиляция "wikilink") с помощью конфигурационной
переменной
[`enable_multi_header`](serve.cfg:problem:enable_multi_header "wikilink").

Если данная переменная установлена в положительное значение, имена
потестовых файлов-заголовков
([`header_pat`](serve.cfg:problem:header_pat "wikilink")),
файлов-хвостов ([`footer_pat`](serve.cfg:problem:footer_pat "wikilink"))
и файлов-опций компиляции
([`compiler_env_pat`](serve.cfg:problem:compiler_env_pat "wikilink"))
будут включать короткое имя языка рограммирования
([`short_name`](serve.cfg:language:short_name "wikilink")).

Значение данной конфигурационной переменной наследуется из абстрактной
задачи, если оно определено в абстрактной задаче и не переопределено в
конкретной задаче.

Поддерживается начиная с версии
[3.5.1](изменения_в_версии_3.5.1 "wikilink")
