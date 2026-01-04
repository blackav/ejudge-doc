Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[ignore_unmarked](Serve.cfg:problem:ignore_unmarked "wikilink")

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Abstract problems"*, поле *"Ignore
unmarked runs in scoring"*, либо страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Concrete problems"*, поле *"Ignore
unmarked runs in scoring"*.

Если данная конфигурационная переменная установлена в 1, в таблице
результатов турнира по системе KIROV учитываются только посылки, у
которых установлен флаг "marked". Посылки, у которых флаг "marked" не
установлен, при построении таблицы результатов турнира игнорируются.

Значение по умолчанию для данной переменной равно 0, то есть все посылки
учитываются при построении таблицы результатов турнира по системе KIROV.

Данная переменная наследуется из абстрактной задачи.
