Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Расширение](Расширение.md)/[Доступ
к ejudge из программ на
Питоне](Доступ_к_ejudge_из_программ_на_Питоне.md)/[Работа с
базой
пользователей](Python:_Работа_с_базой_пользователей.md)/[Проверка
пользователей](Python:_Проверка_пользователей.md).

Запросы данной группы позволяют проверять возможность авторизации
пользователей. Запросы полностью аналогичны запросам на авторизацию, но
запросы на авторизацию должны выполняться для еще неавторизованного
соединения. Запросы на проверку пользователей выполняются для
авторизованного соединения и не приводят к изменению параметров
авторизации соединения.

Для выполнения запросов на проверку пользователей само соединение должно
быть авторизовано с уровнем привилегий ADMIN. Пользователь должен иметь
биты полномочий LIST_USERS для указанного турнира или для всей базы
пользователей.

#### privCheckUser

Для проверки регистрационных логина и пароля пользователя используется
метод privCheckUser

`res = clnt.privCheckUser(`[`ip_str`](Python:ip_str.md)`, `[`ssl_flag`](Python:ssl_flag.md)`, `[`contest_id`](Python:contest_id.md)`, `[`locale_id`](Python:locale_id.md)`, `[`login`](Python:login.md)`, `[`password`](Python:password.md)`)`

Если операция завершилась с ошибкой выбрасывается исключение IOError.
Если операция завершилась успешно, то res - это словарь следующего вида:

`{ 'user_id' : `[`user_id`](Python:user_id.md)`, 'sid' : `[`sid`](Python:sid.md)`, 'name' : `[`name`](Python:name.md)` }`

Возвращаемое имя пользователя name соответствует указанному турниру
contest_id.

#### privCheckUserBySID

Для проверки регистрационного сессионного ключа используется метод
privCheckUserBySID

`res = clnt.privCheckUserBySID(`[`ip_str`](Python:ip_str.md)`, `[`ssl_flag`](Python:ssl_flag.md)`, `[`sid`](Python:sid.md)`)`

Если операция завершилась с ошибкой выбрасывается исключение IOError.
Если операция завершилась успешно, то res - это словарь следующего вида:

`{ 'user_id' : `[`user_id`](Python:user_id.md)`,`  
`  'contest_id' : `[`contest_id`](Python:contest_id.md)`,`  
`  'locale_id' : `[`locale_id`](Python:locale_id.md)`,`  
`  'status_str' : `[`status_str`](Python:status_str.md)`,`  
`  'regflags' : `[`regflags`](Python:regflags.md)`,`  
`  'login' : `[`login`](Python:login.md)`,`  
`  'name' : `[`name`](Python:name.md)` }`

#### privCheckContestUser

Для проверки турнирных логина и пароля пользователя используется метод
privCheckContestUser

`res = clnt.privCheckContestUser(`[`ip_str`](Python:ip_str.md)`, `[`ssl_flag`](Python:ssl_flag.md)`, `[`contest_id`](Python:contest_id.md)`, `[`locale_id`](Python:locale_id.md)`, `[`login`](Python:login.md)`, `[`password`](Python:password.md)`)`

Если операция завершилась с ошибкой выбрасывается исключение IOError.
Если операция завершилась успешно, то res - это словарь следующего вида:

`{ 'user_id' : `[`user_id`](Python:user_id.md)`, 'sid' : `[`sid`](Python:sid.md)`, 'name' : `[`name`](Python:name.md)` }`

Возвращаемое имя пользователя name соответствует указанному турниру
contest_id.

#### privCheckContestUserBySID

Для проверки регистрационного сессионного ключа используется метод
privCheckContestUserBySID

`res = clnt.privCheckContestUserBySID(`[`ip_str`](Python:ip_str.md)`, `[`ssl_flag`](Python:ssl_flag.md)`, `[`sid`](Python:sid.md)`)`

Если операция завершилась с ошибкой выбрасывается исключение IOError.
Если операция завершилась успешно, то res - это словарь следующего вида:

`{ 'user_id' : `[`user_id`](Python:user_id.md)`,`  
`  'contest_id' : `[`contest_id`](Python:contest_id.md)`,`  
`  'locale_id' : `[`locale_id`](Python:locale_id.md)`,`  
`  'status_str' : `[`status_str`](Python:status_str.md)`,`  
`  'regflags' : `[`regflags`](Python:regflags.md)`,`  
`  'login' : `[`login`](Python:login.md)`,`  
`  'name' : `[`name`](Python:name.md)` }`

#### privCheckPrivUser

Для проверки привилегированных пользователей по логину и паролю
используется метод privCheckPrivUser

`res = clnt.privLogin(`[`ip_str`](Python:ip_str.md)`, `[`ssl_flag`](Python:ssl_flag.md)`, `[`contest_id`](Python:contest_id.md)`, `[`locale_id`](Python:locale_id.md)`, `[`priv_role`](Python:priv_role.md)`, `[`login`](Python:login.md)`, `[`password`](Python:password.md)`)`

Если операция завершилась с ошибкой выбрасывается исключение IOError.
Если операция завершилась успешно, то res - это словарь следующего вида:

`{ 'user_id' : `[`user_id`](Python:user_id.md)`, 'sid' : `[`sid`](Python:sid.md)`, 'name' : `[`name`](Python:name.md)` }`

Возвращаемое имя пользователя name соответствует указанному турниру
contest_id. Возможность пользователя user_id войти с указанным уровнем
привилегий, то есть наличие у него битов полномосий MASTER_LOGIN или
JUDGE_LOGIN, не проверяется. Эти проверки должны быть выполнены на
стороне клиента.

#### privCheckPrivUserBySID

Для проверки регистрационного сессионного ключа используется метод
privCheckPrivUserBySID

`res = clnt.privCheckPrivUserBySID(`[`ip_str`](Python:ip_str.md)`, `[`ssl_flag`](Python:ssl_flag.md)`, `[`sid`](Python:sid.md)`)`

Если операция завершилась с ошибкой выбрасывается исключение IOError.
Если операция завершилась успешно, то res - это словарь следующего вида:

`{ 'user_id' : `[`user_id`](Python:user_id.md)`,`  
`  'contest_id' : `[`contest_id`](Python:contest_id.md)`,`  
`  'locale_id' : `[`locale_id`](Python:locale_id.md)`,`  
`  'priv_level' : `[`priv_level`](Python:priv_level.md)`,`  
`  'priv_role' : `[`priv_role`](Python:priv_role.md)`,`  
`  'status_str' : `[`status_str`](Python:status_str.md)`,`  
`  'regflags' : `[`regflags`](Python:regflags.md)`,`  
`  'login' : `[`login`](Python:login.md)`,`  
`  'name' : `[`name`](Python:name.md)` }`
