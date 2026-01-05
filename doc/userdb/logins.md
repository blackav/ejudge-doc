Навигация: [Главная страница](../main_Page.md)/[Система
ejudge](../система_ejudge.md)/[Разработка](../разработка.md)/[Схема
БД пользователей](../схема_БД_пользователей.md)/[Таблица
logins](logins.md)

`CREATE TABLE logins`  
`       (user_id INT UNSIGNED NOT NULL AUTO_INCREMENT PRIMARY KEY, // идентификатор пользователя > 0`  
`       login VARCHAR(64) NOT NULL UNIQUE KEY COLLATE utf8_bin,    // регистрационное имя`  
`       email VARCHAR(128),                                        // e-mail`  
`       pwdmethod TINYINT NOT NULL DEFAULT 0,                      // 0 - plain, 1 - base64, 2 - sha1`  
`       password VARCHAR(64),                                      // пароль`  
`       privileged TINYINT NOT NULL DEFAULT 0,                     // глобальная привилегированность`  
`       invisible TINYINT NOT NULL DEFAULT 0,                      // глобальная невидимость`  
`       banned TINYINT NOT NULL DEFAULT 0,                         // глобальная заблокированность`  
`       locked TINYINT NOT NULL DEFAULT 0,                         // глобальная фиксированность`  
`                                                                  // (глобальные флаги сейчас не используются)`  
`       readonly TINYINT NOT NULL DEFAULT 0,                       // модификация запрещена`  
`       neverclean TINYINT NOT NULL DEFAULT 0,                     // никогда не очищать из БД`  
`       simplereg TINYINT NOT NULL DEFAULT 0,                      // создан по процедуре упрощенной регистрации`  
`       regtime TIMESTAMP DEFAULT CURRENT_TIMESTAMP,               // время регистрации`  
`       logintime TIMESTAMP DEFAULT NULL,                          // время последнего входа`  
`       pwdtime TIMESTAMP DEFAULT NULL,                            // время последней смены регистрационного пароля`  
`       changetime TIMESTAMP DEFAULT NULL                          // время последнего изменения данных`  
`       );`
