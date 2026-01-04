Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[`disable_vm_size_limit`](Serve.cfg:problem:disable_vm_size_limit "wikilink")

Если эта конфигурационная переменная установлена в положительное
значение, при тестировании решений не будет устанавливаться ограничение
на максимальный размер виртуальной памяти
[`max_vm_size`](Serve.cfg:problem:max_vm_size "wikilink").

Опцию
[`disable_vm_size_limit`](Serve.cfg:problem:disable_vm_size_limit "wikilink")
следует использовать вместе с опцией
[`max_rss_size`](Serve.cfg:problem:max_rss_size "wikilink"). Таким
образом, вместо ограничения на максимальный размер виртуального
адресного пространства процесса будет устанавливаться ограничение на
объем использованной оперативной памяти процесса.

Значение переменной наследуется из абстрактной задачи.

Пример.

`[problem]`  
`# ...`  
`disable_vm_size_limit`  
`max_rss_size = 256M`

Поддерживается начиная с версии
[3.12.0](изменения_в_версии_3.12.0 "wikilink").
