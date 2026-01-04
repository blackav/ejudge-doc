Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
языков](serve.cfg:language "wikilink")/[`preserve_line_numbers`](Serve.cfg:language:preserve_line_numbers "wikilink")

Данный конфигурационный параметр позволяет изменить режим сохранения
исходных номеров строк, задаваемый глобальным конфигурационным
параметром
[`preserve_line_numbers`](Serve.cfg:global:preserve_line_numbers "wikilink"),
для данного языка.

Если конфигурационный параметр
[`preserve_line_numbers`](Serve.cfg:language:preserve_line_numbers "wikilink")
в разделе языка программирования не определён, используется значение
глобального параметра
[`preserve_line_numbers`](Serve.cfg:global:preserve_line_numbers "wikilink")
(по умолчанию 0). Если же конфигурационный параметр
[`preserve_line_numbers`](Serve.cfg:language:preserve_line_numbers "wikilink")
определён в неотрицательное значение, будет использоватся это значение.

В итоге если режим сохранения исходных номеров строк для данного языка
установлен в положительное значение, программы на скриптовых языках
будут обрабатываться таким образом, что номера строк при выполнении
программы будут соответствовать номерам строк в сданном программе.

Поддерживается начиная с версии
[3.12.0](изменения_в_версии_3.12.0 "wikilink").
