Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Разработка](Разработка "wikilink")/[Схема
БД пользователей](Схема_БД_пользователей "wikilink")/[Таблица
users](userdb:users "wikilink")

`CREATE TABLE users`  
`       (user_id INT UNSIGNED NOT NULL,                 // идентификатор пользователя`  
`       contest_id INT UNSIGNED NOT NULL,               // идентификатор турнира`  
`       cnts_read_only TINYINT NOT NULL DEFAULT 0,      // 1 - изменение запрещено`  
`       instnum INT NOT NULL,                           // номер учебного заведения (-1 - неопределен)`  
`       username VARCHAR(512),                          // имя пользователя`  
`       pwdmethod TINYINT NOT NULL DEFAULT 0,           // 0 - plain, 1 - base64, 2 - sha1`  
`       password VARCHAR(128),                          // пароль`  
`       pwdtime TIMESTAMP DEFAULT 0,                    // время последней смены пароля`  
`       createtime TIMESTAMP DEFAULT CURRENT_TIMESTAMP, // время создания`  
`       changetime TIMESTAMP DEFAULT 0,                 // время последнего изменения`  
`       logintime TIMESTAMP DEFAULT 0,                  // время последнего входа в турнир`  
`       inst VARCHAR(512),                              // учебное заведение`  
`       inst_en VARCHAR (512),                          // учебное заведение (на англ.)`  
`       instshort VARCHAR (512),                        // краткое название учебного заведения`  
`       instshort_en VARCHAR (512),                     // краткое название учебного заведения (на англ.)`  
`       fac VARCHAR(512),`  
`       fac_en VARCHAR (512),`  
`       facshort VARCHAR (512),`  
`       facshort_en VARCHAR (512),`  
`       homepage VARCHAR (512),`  
`       phone VARCHAR (512),`  
`       city VARCHAR (512),`  
`       city_en VARCHAR (512),`  
`       region VARCHAR (512),`  
`       area VARCHAR (512),`  
`       zip VARCHAR (512),`  
`       street VARCHAR (512),`  
`       country VARCHAR (512),`  
`       country_en VARCHAR (512),`  
`       location VARCHAR (512),`  
`       spelling VARCHAR (512),`  
`       printer VARCHAR (512),`  
`       languages VARCHAR (512),`  
`       exam_id VARCHAR (512),`  
`       exam_cypher VARCHAR (512),`  
`       field0 VARCHAR(512),`  
`       field1 VARCHAR(512),`  
`       field2 VARCHAR(512),`  
`       field3 VARCHAR(512),`  
`       field4 VARCHAR(512),`  
`       field5 VARCHAR(512),`  
`       field6 VARCHAR(512),`  
`       field7 VARCHAR(512),`  
`       field8 VARCHAR(512),`  
`       field9 VARCHAR(512),`  
`       PRIMARY KEY (user_id, contest_id),`  
`       FOREIGN KEY (user_id) REFERENCES `[`logins`](userdb:logins "wikilink")` (user_id)`  
`       );`
