Навигация: [Главная страница](../main_Page.md)/[Система
ejudge](../система_ejudge.md)/[Разработка](../разработка.md)/[Схема
БД пользователей](../схема_БД_пользователей.md)/[Таблица
cntsregs](cntsregs.md)

`CREATE TABLE cntsregs`  
`       (user_id INT UNSIGNED NOT NULL,                 // идентификатор пользователя`  
`       contest_id INT UNSIGNED NOT NULL,               // идентификатор турнира`  
`       status TINYINT NOT NULL DEFAULT 0,              // статус: 0 - ok, 1 - pending, 2 - rejected`  
`       banned TINYINT NOT NULL DEFAULT 0,              // 1, если забанен`  
`       invisible TINYINT NOT NULL DEFAULT 0,           // 1, если невидим`  
`       locked TINYINT NOT NULL DEFAULT 0,              // 1, если блокирован`  
`       incomplete TINYINT NOT NULL DEFAULT 0,          // 1, если регистрация неполна`  
`       disqualified TINYINT NOT NULL DEFAULT 0,        // 1, если дисквалифицирован`  
`       createtime TIMESTAMP DEFAULT CURRENT_TIMESTAMP, // дата создания`  
`       changetime TIMESTAMP DEFAULT 0,                 // дата изменения`  
`       PRIMARY KEY (user_id, contest_id),`  
`       FOREIGN KEY (user_id) REFERENCES `[`logins`](logins.md)` (user_id)`  
`       );`
