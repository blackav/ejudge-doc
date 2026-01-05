priv_role - это роль, выполняемая пользователем. Поддерживаются
следующие роли:

` 0 CONTESTANT,`  
` 1 OBSERVER,`  
` 2 EXAMINER,`  
` 3 CHIEF_EXAMINER,`  
` 4 COORDINATOR,`  
` 5 JUDGE,`  
` 6 ADMIN,`

В текущей версии поддерживаются только численные значения ролей от 0 до
6. Роли CONTESTANT соответствует уровень привилегий USER. Ролям
OBSERVER - JUDGE соответствует уровню привилегий JUDGE. Роли ADMIN
соответствует уровень привилегий ADMIN.

См. также [priv_level](Python:priv_level.md).
