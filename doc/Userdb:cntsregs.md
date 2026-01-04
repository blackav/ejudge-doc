Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Разработка](Разработка "wikilink")/[Схема
БД пользователей](Схема_БД_пользователей "wikilink")/[Таблица
cntsregs](userdb:cntsregs "wikilink")

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
`       FOREIGN KEY (user_id) REFERENCES `[`logins`](userdb:logins "wikilink")` (user_id)`  
`       );`
