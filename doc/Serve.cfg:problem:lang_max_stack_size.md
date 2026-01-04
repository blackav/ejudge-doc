Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[`lang_max_stack_size`](serve.cfg:problem:lang_max_stack_size "wikilink")

Данная конфигурационная переменная позволяет установить ограничение
размера стека специально для решений на некотором языке
программирования. Например,

`[problem]`  
`...`  
`max_stack_size = 32M`  
`lang_max_stack_size = "python3=64M"`  
`lang_max_stack_size = "kumir=128M"`

Устанавливает ограничение на размер стека в 32 мегабайта, но для
программ на языке python3 ограничение устанавливается в 64 мегабайта, а
для программ на языке kumir — 128 мегабайт.
