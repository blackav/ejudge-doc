Навигация: [Главная страница](Main_Page.md)/[Система
ejudge](Система_ejudge.md)/[Использование](Использование.md)/[API](API.md)/[submit-run-input
(привилегированный)](API:priv:submit-run-input.md)

Запрос отправляет на проверку файл с исходным кодом и тестовые данные,
на которых файл должен запускаться.

Уровень доступа: администратор в контесте (аутентификация с помощью API
key или EJSID/session_id).

Method: POST

Content-type: multipart/form-data

Параметры:

- `contest_id` (int) - идентификатор турнира
- `action` (string) — строка `submit-run-input`
- `sender_user_login` (string, optional) — логин пользователя, от имени
  которого выполняется посылка
- `sender_user_id` (int, optional) — user id пользователя (если не задан
  sender_user_login)
- `sender_ip` (string, optional) — IP-адрес отправителя
- `sender_ssl_flag` (int, optional) — 1, если протокол HTTPS; 0, если
  HTTP
- `prob_id` (string или int) — либо short_name (string) задачи, либо
  internal_name (string) задачи, либо id (int) задачи
- `lang_id` (string или int) — либо short_name (string) языка
  программирования, либо id (int) языка программирования
- `eoln_type` (int, optional) — тип преобразования концов строк
- `file` (string) — исходный код программы
- `text_form` (string) — исходный код программы (альтернатива для file)
- `file_input` (string) — входные данные для программы
- `text_form_input` (string) — входные данные для программы
  (альтернатива для file_input)
- `ext_user_kind`, `ext_user` — [внешний идентификатор
  пользователя](Внешние_идентификаторы_пользователей.md)
  ([3.11.0](Изменения_в_версии_3.11.0.md)).
- `notify_driver`, `notify_kind`, `notify_queue` — [идентификатор
  очереди сообщений](Нотификации_во_внешние_системы.md)
  ([3.11.0](Изменения_в_версии_3.11.0.md)).

Response content type: application/json

В случае ошибки возвращается JSON:

`{`  
`  "ok": false,`  
`  "server_time": UNIX-TIMESTAMP,`  
`  "action": "submit-run-input",`  
`  "error": {`  
`    "num": ERROR-CODE,`  
`    "symbol": ERROR-SYMBOL,`  
`    "message": ERROR-MESSAGE`  
`  }`  
`}`

В случае успеха возвращается JSON:

`{`  
`  "ok": true,`  
`  "result": {`  
`    "submit_id": ID`  
`  }`  
`}`

Возвращается ID (int64), который следует использовать для запроса
статуса посылки.
