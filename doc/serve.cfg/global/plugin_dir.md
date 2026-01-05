Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Глобальные
конфигурационные
параметры](serve.cfg:global.md)/[`plugin_dir`](Serve.cfg:global:plugin_dir.md)

**Редактирование элемента:** страница *"Editing contest"*, вкладка
*"Global settings (serve.cfg)"*, блок *"Files and directories"*, поле
*"Directory for problem plugins (relative to contest configuration
dir)"*.

Переменная позволяет задать базовый каталог для подгружаемых модулей
задач. Значение этой переменной по умолчанию - `"../plugins"`, то есть
подгружаемые модули задач должны находиться в каталоге "plugins"
каталога турнира (на одном уровне с каталогами "conf", "checkers",
"tests" и т. д.).
