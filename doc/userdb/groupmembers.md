Навигация: [Главная страница](../main_Page.md)/[Система
ejudge](../система_ejudge.md)/[Разработка](../разработка.md)/[Схема
БД пользователей](../схема_БД_пользователей.md)/[Таблица
groupmembers](groupmembers.md)

CREATE TABLE \`groupmembers\`

``  (`group_id` int(11) NOT NULL,         //идентификатор группы ``  
``  `user_id` int(11) NOT NULL,           //идентификатор пользователя, входящего в группу ``  
``  `rights` varchar(512) DEFAULT NULL,   //? ``  
``  PRIMARY KEY (`group_id`,`user_id`), ``  
``  KEY `u` (`user_id`)); ``
