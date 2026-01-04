Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Разработка](Разработка "wikilink")/[Схема
БД пользователей](Схема_БД_пользователей "wikilink")/[Таблица
participants](userdb:participants "wikilink")

`CREATE TABLE participants`  
`       (serial INT UNSIGNED NOT NULL AUTO_INCREMENT PRIMARY KEY, // идентификатор члена команды, больше 0`  
`       user_id INT UNSIGNED NOT NULL,                            // идентификатор пользователя, больше 0`  
`       contest_id INT UNSIGNED NOT NULL,                         // идентификатор турнира, больше 0`  
`       team_role TINYINT NOT NULL,                               // 0 - участник, 1 - запасной и т. д.`  
`       createtime TIMESTAMP DEFAULT CURRENT_TIMESTAMP,           // время создания`  
`       changetime TIMESTAMP DEFAULT 0,                           // время последнего изменения`  
`       firstname VARCHAR(512),`  
`       firstname_en VARCHAR(512),`  
`       middlename VARCHAR(512),`  
`       middlename_en VARCHAR(512),`  
`       surname VARCHAR(512),`  
`       surname_en VARCHAR(512),`  
`       status TINYINT NOT NULL,`  
`       gender TINYINT NOT NULL,`  
`       grade TINYINT NOT NULL,`  
`       grp VARCHAR(512),`  
`       grp_en VARCHAR(512),`  
`       occupation VARCHAR(512),`  
`       occupation_en VARCHAR(512),`  
`       discipline VARCHAR(512),`  
`       email VARCHAR(512),`  
`       homepage VARCHAR(512),`  
`       phone VARCHAR(512),`  
`       inst VARCHAR(512),`  
`       inst_en VARCHAR(512),`  
`       instshort VARCHAR(512),`  
`       instshort_en VARCHAR(512),`  
`       fac VARCHAR(512),`  
`       fac_en VARCHAR(512),`  
`       facshort VARCHAR(512),`  
`       facshort_en VARCHAR(512),`  
`       birth_date DATE DEFAULT NULL,`  
`       entry_date DATE DEFAULT NULL,`  
`       graduation_date DATE DEFAULT NULL,`  
`       );`
