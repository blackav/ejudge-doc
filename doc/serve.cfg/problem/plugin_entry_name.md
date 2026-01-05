Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[Конфигурационные
файлы](Конфигурационные_файлы.md)/[serve.cfg](serve.cfg.md)/[Конфигурационные
параметры
задач](serve.cfg:problem.md)/[`plugin_entry_name`](Serve.cfg:problem:plugin_entry_name.md)

С помощью данного конфигурационного параметра можно задать имя
переменной-структуры, являющейся точкой входа в плагин задачи, который
задаётся с помощью
[`plugin_file`](serve.cfg:problem:plugin_file.md).

Например, в случае

`[problem]`  
`# ...`  
`plugin_entry_name = "testname"`

Точка входа в плагин задачи должна быть описана в плагине примерно
следующим образом:

`struct problem_plugin_iface plugin_problem_testname =`  
`{`  
`    {`  
`        sizeof(struct problem_plugin_iface),`  
`        EJUDGE_PLUGIN_IFACE_VERSION,`  
`        "problem",`  
`        "testname",`  
`    },`  
`    PROBLEM_PLUGIN_IFACE_VERSION,`  
`// ...`

Поддерживается начиная с версии
[3.12.0](изменения_в_версии_3.12.0.md).
