Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Конфигурационные
параметры
задач](serve.cfg:problem.md)/[`lang_compiler_env`](serve.cfg:problem:lang_compiler_env.md)

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
