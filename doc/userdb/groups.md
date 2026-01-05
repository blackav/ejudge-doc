Навигация: [Главная страница](../main_Page.md)/[Система
ejudge](../система_ejudge.md)/[Разработка](../разработка.md)/[Схема
БД пользователей](../схема_БД_пользователей.md)/[Таблица
groups](groups.md)

`` CREATE TABLE `groups` ``  
``  (`group_id` int(11) NOT NULL AUTO_INCREMENT,    //идентификатор группы ``  
``  `group_name` varchar(128) NOT NULL,             //название группы ``  
``  `description` varchar(512) DEFAULT NULL,        //описание ``  
``  `created_by` int(11) NOT NULL,                  //id пользователя - создателя группы ``  
``  `create_time` datetime NOT NULL,                //дата создания группы ``  
``  `last_change_time` datetime DEFAULT NULL,       //дата последнего изменения группы ``  
``  PRIMARY KEY (`group_id`), ``  
``  UNIQUE KEY `group_name` (`group_name`), ``  
``  KEY `created_by` (`created_by`)); ``
