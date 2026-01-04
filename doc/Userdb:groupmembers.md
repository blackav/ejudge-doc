Навигация: [Главная страница](Main_Page "wikilink")/[Система
ejudge](Система_ejudge "wikilink")/[Разработка](Разработка "wikilink")/[Схема
БД пользователей](Схема_БД_пользователей "wikilink")/[Таблица
groupmembers](userdb:groupmembers "wikilink")

CREATE TABLE \`groupmembers\`

``  (`group_id` int(11) NOT NULL,         //идентификатор группы ``  
``  `user_id` int(11) NOT NULL,           //идентификатор пользователя, входящего в группу ``  
``  `rights` varchar(512) DEFAULT NULL,   //? ``  
``  PRIMARY KEY (`group_id`,`user_id`), ``  
``  KEY `u` (`user_id`)); ``
