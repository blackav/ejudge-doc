Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[advance_to_next](serve.cfg:problem:advance_to_next "wikilink")

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
