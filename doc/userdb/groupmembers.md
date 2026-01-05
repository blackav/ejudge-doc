Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Разработка](Разработка.md)/[Схема
БД пользователей](Схема_БД_пользователей.md)/[Таблица
groupmembers](userdb:groupmembers.md)

CREATE TABLE \`groupmembers\`

``  (`group_id` int(11) NOT NULL,         //идентификатор группы ``  
``  `user_id` int(11) NOT NULL,           //идентификатор пользователя, входящего в группу ``  
``  `rights` varchar(512) DEFAULT NULL,   //? ``  
``  PRIMARY KEY (`group_id`,`user_id`), ``  
``  KEY `u` (`user_id`)); ``
