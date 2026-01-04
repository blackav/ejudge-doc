Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[`checker_env`](serve.cfg:problem:checker_env "wikilink")

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Concrete problems"*, поле *"Checker
environment"*.

Данная конфигурационная переменная задачи позволяет устанавливать
переменные окружения для запуска проверяющей программы. Например,

`checker_env="VAR1=1"`  
`checker_env="VAR2=2"`

При вызове проверяющей программы будут дополнительно установлены
переменные окружения `VAR1` и `VAR2`.
