Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Конфигурационные
параметры
задач](serve.cfg:problem.md)/[advance_to_next](serve.cfg:problem:advance_to_next.md)

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Abstract problems"*, поле
*"Automatically advance to the next problem"*, либо страница *"Editing
contest"*, вкладка *"Problems (serve.cfg)"*, блок *"Concrete problems"*,
поле *"Automatically advance to the next problem"*.

Данная переменная работает только для задач типа `select-one` (выбор
одного ответа из нескольких данных). Если значение переменной не равно
0, после сдачи задачи (то есть нажатия на кнопку "Submit" или щелчка
мыши на варианте ответа для упрощенного режима (`exam_mode`)) происходит
автоматический переход на следующую задачу. Значение переменной
наследуется от абстрактной задачи.
