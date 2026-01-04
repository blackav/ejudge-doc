Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[`lang_compiler_env`](serve.cfg:problem:lang_compiler_env "wikilink")

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Concrete problems"*, поле *"Compiler
environment"*.

Данная конфигурационная переменная позволяет задавать переменные
окружения, которые будут установлены при компиляции посылки. Например,

`[problem]`  
`...`  
`lang_compiler_env="gcc=EJUDGE_FLAGS=-Wall -O2"`  
`lang_compiler_env="gcc=VAR1=1"`  
`lang_compiler_env="g++=EJUDGE_FLAGS=-std=gnu++0x"`

Для данной задачи при использовании языка gcc для скрипта компиляции
будут установлены переменные окружения EJUDGE_FLAGS и VAR1, а при
использовании языка g++ переменная окружения EJUDGE_FLAGS.

Поддерживается с версии 2.3.20.
