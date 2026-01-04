Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Разработка](Разработка.md)/[Схема
БД пользователей](Схема_БД_пользователей.md)/[Таблица
cookies](userdb:cookies.md)

`CREATE TABLE cookies`  
`       (cookie VARCHAR(32) NOT NULL PRIMARY KEY,     // случайное 64-битное число (кроме 0), хранится в 16-ричном виде (16 цифр)`  
`       user_id INT NOT NULL,                         // идентификатор пользователя`  
`       contest_id INT UNSIGNED NOT NULL,             // идентификатор турнира`  
`       priv_level TINYINT NOT NULL DEFAULT 0,        // уровень привилегий`  
`       role_id TINYINT NOT NULL DEFAULT 0,           // роль пользователя`  
`       ip_version TINYINT NOT NULL DEFAULT 4,        // версия IP-протокола поля IP`  
`       locale_id TINYINT NOT NULL DEFAULT 0,         // идентификатор локали`  
`       recovery TINYINT NOT NULL DEFAULT 0,          // используется для восстановления пароля`  
`       team_login TINYINT NOT NULL DEFAULT 0,        // использован при входе в турнир`  
`       ip VARCHAR(64) NOT NULL,                      // IP-адрес`  
`       ssl_flag TINYINT NOT NULL DEFAULT 0,          // флаг доступа по SSL`  
`       expire DATETIME NOT NULL,                     // дата истечения ключа`  
`       FOREIGN KEY (user_id) REFERENCES `[`logins`](userdb:logins.md)` (user_id)`  
`       );`
