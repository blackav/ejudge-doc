Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Использование](Использование "wikilink")/[Конфигурационные
файлы](Конфигурационные_файлы "wikilink")/[serve.cfg](serve.cfg "wikilink")/[Конфигурационные
параметры
задач](serve.cfg:problem "wikilink")/[`acm_run_penalty`](Serve.cfg:problem:acm_run_penalty "wikilink")

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Abstract problems"*, поле *"Penalty for
a submission (minutes)"*, либо страница *"Editing contest"*, вкладка
*"Problems (serve.cfg)"*, блок *"Concrete problems"*, поле *"Penalty for
a submission (minutes)"*.

Данная конфигурационная переменная действует только в режимах турнира
*ACM* или *MOSCOW* и позволяет задавать штраф за неправильные попытки до
сдачи задачи. Стандартное значение штрафа, используемое на всех
соревнованиях по системе *ACM* равно 20. Например, можно установить
значение штрафа в 0, чтобы принимать задачи по системе "сдана/не сдана".

Переменная `acm_run_penalty` может быть определена в абстрактной задаче,
в это случае ее значение наследуется.
