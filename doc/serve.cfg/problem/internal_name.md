Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Конфигурационные
параметры
задач](serve.cfg:problem.md)/[internal_name](serve.cfg:problem:internal_name.md)

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Concrete problems"*, поле *"Internal
name"*.

Значение данной переменной может использоваться в качестве компоненты
пути к тестам или проверяющим программам. Этой переменной соответствует
форматная подстановка `%PL`. Пример использования:

`[problem]`  
`short_name = "A"`  
`internal_name = "abc"`  
`long_name = "An Abc problem"`  
`test_dir = "%PL"`

В этом случае файлы с тестами будут размещаться не в каталоге `tests/A`,
а в каталоге `tests/abc`.
