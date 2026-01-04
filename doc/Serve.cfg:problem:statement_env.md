Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[`statement_env`](serve.cfg:problem:statement_env "wikilink")

Данная конфигурационная переменная позволяет задать переменные, которые
будут подставлены при отображении условия задачи из XML-файла условия
задачи [statement.xml](statement.xml "wikilink").

Например, если в конфигурационном файле заданы

`statement_env = "VAR1=block"`  
`statement_env = "VAR2=Some text"`

А в файле с условием задачи:

`<div style="display: ${VAR1:-none};">`  
`<p>Note: ${VAR2}.</p>`  
`</div>`  
`<div style="display: ${VAR3:-none};">`  
`<p>Note: ${VAR4}.</p>`  
`</div>`

Будет выполнена подстановка, после которой условие задачи примет
следующий вид:

`<div style="display: block;">`  
`<p>Note: Some text.</p>`  
`</div>`  
`<div style="display: none;">`  
`<p>Note: .</p>`  
`</div>`

Поддерживается с версии [3.6.1](изменения_в_версии_3.6.1 "wikilink").
