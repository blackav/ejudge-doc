Навигация: [Главная страница](../main_Page.md)/[Система
ejudge](../система_ejudge.md)/[Использование](../использование.md)/[Конфигурационные
файлы](../конфигурационные_файлы.md)/[ejudge.xml](../ejudge.xml.md)/[`caps_file`](caps_file.md)

Данный элемент позволяет задать имя XML-файла, содержащего информацию о
глобальных полномочиях пользователей. Если этот файл изменился, то его
обновленное содержимое будет загружено в систему ejudge на лету, не
требуя перезапуска ejudge.

`<caps_file>capabilities.xml</caps_file>`

Если в элементе задан относительный путь, то базовым каталогом для
поиска этого файла будет каталог, в котором находится файл ejudge.xml.
Так, в примере выше, если файл ejudge.xml находится в каталоге
/home/judges/data, полный путь к файлу capabilities.xml должен быть
/home/judges/data/capabilities.xml.

Файл capabilities.xml должен содержать корневой элемент `<config>`, в
который вложены элементы
`<`[`user_map`](user_map.md)`>` и
`<`[`caps`](caps.md)`>`.

`<config>`  
`  <`[`user_map`](user_map.md)`>`  
`    <`[`map`](map.md)` system_user="user1" local_user="user1" />`  
`  </user_map>`  
`  <`[`caps`](caps.md)`>`  
`    <`[`cap`](cap.md)` login="user1">`  
`      MASTER_LOGIN,JUDGE_LOGIN,LIST_USERS,CREATE_USER,GET_USER,`  
`      EDIT_USER,DELETE_USER,PRIV_EDIT_USER,PRIV_DELETE_USER,`  
`      EDIT_CONTEST,DUMP_USERS,EDIT_PASSWD,PRIV_EDIT_PASSWD,`  
`    </cap>`  
`  </caps>`  
`</config>`
